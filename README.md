# Email Signatures Project

Centralized email signature templates for multiple organizations.
Each company gets a folder with its HTML signature template + customization notes.

## Organizations

| Company | Domain | Industry | Folder | Logo URL | Status |
|---|---|---|---|---|---|
| Qualitas Material Testing Laboratories | qualitasme.com | Materials testing lab (ISO 17025, ENAS\|EIAC) — Abu Dhabi & Dubai | [qualitas/](qualitas/) | `https://www.qualitasme.com/logo.png` ✅ live | ✅ v4 complete + generator |
| Chemparts Middle East FZC | chemparts-me.com | Distributor — analytical instruments & lab equipment — SAIF Zone Sharjah & Abu Dhabi | [chemparts/](chemparts/) | `https://chemparts-me.com/images/logo.jpeg` ✅ live | ✅ v1 complete + generator |
| Spectrum Inspection & Testing Services | speclabuae.com | Petroleum testing lab (ASTM/ISO) — UAE | _(pending)_ | `https://speclabuae.com/assets/images/logo.png` ⚠️ **SSL cert expired** | **BLOCKED** — renew SSL first |
| _(add next org here)_ | | | | | |

## How signatures are built

- **HTML + inline CSS, table-based layout** — required for email client compatibility (Outlook, Gmail, Apple Mail).
- **Placeholders** in `{{DOUBLE_BRACES}}` — users edit only their name, designation, phone, email.
- **Hosted images** — logo and UAE flag GIF must live at a public URL (company website, CDN, or GitHub raw). Embedded base64 images get stripped by many clients, especially Outlook.
- **UAE patriotic banner** — small animated UAE flag + tagline "Proudly standing with the UAE — our home of growth, resilience and unity." appears at the bottom of every org's signature.

## Shared mailboxes

Some teams share an inbox but each user has the same designation
(e.g. multiple sales reps under `sales@`). For these, the signature is identical
except for the **Name** line — users just paste the template and change one field.

## Workflow

1. Draft signature HTML in `<org>/signature.html`
2. Preview in `<org>/preview.html` (open in browser to check rendering)
3. Update `<org>/INSTALL.md` with the user-facing instructions
4. Send install link / file to users
5. Update this README's status column

## Mail platform — Zoho Mail

All organizations run on **Zoho Mail**. This unlocks two delivery paths for the signature:

1. **Org-wide signature (recommended)** — Zoho Mail Admin Console → *Mail Settings → Organization Signature*. Set the HTML once, applied server-side to every outbound mail for every user in that org. Uses directory placeholders (e.g. display name, title, mobile) so each user gets their own details auto-filled. Users cannot accidentally remove or break it.
2. **Per-user install (fallback)** — for staff using Zoho Mail in Outlook/Apple Mail/mobile clients where the org-wide signature may not get appended, fall back to the manual install guide in each `<org>/INSTALL.md`.

## Asset hosting — GitHub

Repo: **https://github.com/itqualitasme-lgtm/mail-sign** (public)
Cloned working copy on this machine: `C:\Users\razin\AppData\Local\Temp\mail-sign-work\mail-sign`
Push access: SSH key on this laptop is registered to GitHub user `razinahmed`, who can push directly to the repo.

Asset URL pattern (used inside every `signature.html`):
```
https://raw.githubusercontent.com/itqualitasme-lgtm/mail-sign/main/<folder>/<file>
```

The repo MUST stay public — making it private breaks every signature in every recipient's inbox immediately.

## Open items

- [x] ~~GitHub repo public + populated~~
- [x] ~~Qualitas template + generator + install guide~~ (v4 — letter template, white-card defense)
- [x] ~~UAE flag GIF uploaded to common/~~ (763 KB — could be optimized later)
- [x] ~~Chemparts template + generator + install guide~~ (v1 — same v4 pattern, navy brand)
- [ ] **Renew SSL cert on speclabuae.com** — currently expired, blocks Speclab work
- [ ] Build Speclab signature template once SSL is fixed
- [ ] Optimize UAE flag GIF: 763 KB → ~50 KB (resize to ~60×40 px, fewer frames)
- [ ] Test Qualitas signature in actual recipient clients (especially Gmail web in dark mode) to confirm v4 white-card defense holds
- [ ] Confirm tagline wording with management
- [ ] Continue collecting remaining organization domains
- [ ] Optional: build a unified `generator.html` at repo root with company picker (currently each org has its own copy)
