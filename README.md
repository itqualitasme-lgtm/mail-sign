# mail-sign

Email signature assets and HTML templates for itqualitasme organizations.

## What's in here

```
mail-sign/
├── common/                ← shared assets used by every organization
│   └── uae-flag.gif       (animated UAE flag — used in patriotic banner)
├── qualitas/              ← Qualitas Material Testing Laboratories
│   ├── logo.png
│   └── signature.html
├── chemparts/             ← Chemparts Middle East FZC
│   ├── logo.jpeg
│   └── signature.html
└── speclab/               ← Spectrum Inspection & Testing Services
    ├── logo.png
    └── signature.html
```

## How email signatures use these files

Each `signature.html` references its images using **raw GitHub URLs** so that
any email client (Outlook, Gmail, Apple Mail, Zoho, mobile apps) can fetch them
anonymously over HTTPS:

```html
<img src="https://raw.githubusercontent.com/itqualitasme-lgtm/mail-sign/main/qualitas/logo.png" />
<img src="https://raw.githubusercontent.com/itqualitasme-lgtm/mail-sign/main/common/uae-flag.gif" />
```

The repo **must stay public** for these URLs to work — making it private breaks
every signature in every recipient's inbox immediately.

## Updating an asset

1. Open the file in GitHub → click the pencil icon → upload a new version, or
2. Use **Add file → Upload files** to drag a new file in.

After committing, the new image is live within ~1 minute (raw.githubusercontent.com cache).

> Filename matters. If you upload `logo-v2.png` instead of replacing `logo.png`,
> the signature will still point at the old file. Always overwrite the same filename
> unless you also update the `<img src=...>` in `signature.html`.

## Mail platform

All organizations run on **Zoho Mail**. The plan is to deploy these signatures
via the Zoho Mail Admin Console **Organization Signature** feature, which appends
them server-side to every outgoing message and pulls user details (name, title,
mobile) from the Zoho directory.

A per-user manual install fallback (for Outlook desktop, OWA, Gmail, Apple Mail)
lives alongside each organization's `signature.html` as `INSTALL.md`.
