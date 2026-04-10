# Qualitas Email Signature — Installation Guide

This guide is for **end users**. Send this file (or copy/paste it) to staff
along with the `signature.html` file.

---

## Step 1 — Customize your details

1. Open `signature.html` in **Notepad** (right-click → Open with → Notepad).
2. Find the four lines marked `<!-- EDIT -->` and change only the text after them:
   - **Name** — your full name
   - **Designation** — your job title
   - **Mob** — your mobile number (also update the `tel:` link)
   - **Email** — your email address (also update the `mailto:` link)
3. **Do not change** anything else — table tags, colors, widths. The layout
   will break in Outlook if you do.
4. Save the file.

> **Shared mailboxes (sales@, info@, account@, etc.):** Only change the
> **Name** line. Designation, phone, and email stay the same for everyone
> on that mailbox.

---

## Step 2 — Preview it

Double-click `signature.html` — it opens in your browser so you can see
exactly how it will look in an email.

---

## Step 3 — Install in your email client

### Zoho Mail (web — mail.zoho.com) ★ recommended for our org

1. Open `signature.html` in your browser, **Ctrl + A**, **Ctrl + C**.
2. Log into Zoho Mail → click the **Settings gear** (top right) → **Settings**.
3. In the left sidebar, click **Signatures**.
4. Click **Add** (or the **+** button) to create a new signature.
5. Give it the name `Qualitas` and select the email account it applies to.
6. Click into the large editor area, then click the **`<>` Source** / **HTML** button in the toolbar (it switches the editor from rich-text to raw HTML mode — this step is important, otherwise pasting will mangle the layout).
7. **Ctrl + V** to paste the signature HTML.
8. Click the **`<>` Source** button again to switch back to preview mode and check the layout looks right.
9. Under **Signature Settings**, set the new `Qualitas` signature as the default for the account.
10. Click **Save**.
11. Open a new compose window — your signature should appear automatically.

> **For org-wide deployment:** if you're an admin and want to push this to every
> user without each person installing it manually, see the *Zoho Mail Admin
> Console → Mail Settings → Organization Signature* feature instead. This applies
> the signature server-side to every outbound message and pulls user details
> (name, title, mobile) from the Zoho directory automatically.

### Outlook (desktop — Windows)

1. Open `signature.html` in your browser.
2. Press **Ctrl + A** to select everything, then **Ctrl + C** to copy.
3. In Outlook: **File → Options → Mail → Signatures…**
4. Click **New**, name it `Qualitas`, click **OK**.
5. Click inside the big edit box and press **Ctrl + V** to paste.
6. Under **Choose default signature** on the right:
   - **New messages:** Qualitas
   - **Replies/forwards:** Qualitas
7. Click **OK**. Done — open a new mail to test.

### Outlook on the Web (OWA / Office 365 webmail)

1. Open `signature.html` in your browser, **Ctrl + A**, **Ctrl + C**.
2. In OWA, click the **gear icon** (top right) → **View all Outlook settings**.
3. **Mail → Compose and reply → Email signature**.
4. Click **+ New signature**, name it `Qualitas`.
5. Click in the edit box and **Ctrl + V** to paste.
6. Under **Select default signatures**, set Qualitas for both new messages and replies.
7. **Save**.

### Gmail / Google Workspace

1. Open `signature.html` in Chrome, **Ctrl + A**, **Ctrl + C**.
2. In Gmail, click the **gear icon** → **See all settings**.
3. Scroll down to **Signature**, click **+ Create new**, name it `Qualitas`.
4. Click in the edit box and **Ctrl + V** to paste.
5. Under **Signature defaults**, pick Qualitas for **For New Emails Use** and **On Reply/Forward Use**.
6. Scroll to the bottom and click **Save Changes**.

### Apple Mail (Mac)

1. Open `signature.html` in Safari, **Cmd + A**, **Cmd + C**.
2. Mail → **Settings → Signatures**.
3. Pick your account, click **+** to add a new signature, name it `Qualitas`.
4. Click in the right pane, **Cmd + V** to paste.
5. **Uncheck** "Always match my default message font" (very important —
   otherwise Mail strips the formatting).
6. At the bottom, set **Choose Signature** to Qualitas.
7. Close the window.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Logo / UAE flag shows as a broken image | The image URL is wrong or the host is down. Contact IT. |
| Layout looks stacked / squished in Outlook | You edited something other than the `<!-- EDIT -->` lines. Start over with a fresh `signature.html`. |
| Colors look wrong in dark mode | Some clients invert colors automatically — this is normal and unavoidable. |
| Apple Mail strips the formatting | You forgot Step 5 — uncheck "Always match my default message font". |
| Outlook shows a red X instead of the logo | Outlook is blocking remote images. Click **Download Pictures** in the message, or whitelist the image domain. |

---

## Need help?

Contact IT: **it.admin@qualitasme.com**
