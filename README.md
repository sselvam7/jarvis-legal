# jarvis-legal

Legal documents for **JARVIS** — a personal AI SMS assistant operated by Surya.

## What this repo is

This repository contains the static HTML legal pages required for Twilio 10DLC
compliance:

| File | Purpose |
|---|---|
| `index.html` | Landing page with links to both legal documents |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms & Conditions |
| `_redirects` | Cloudflare Pages rewrite rules (`/privacy` → `privacy.html`, etc.) |
| `_headers` | Cloudflare Pages HTTP headers (Cache-Control for HTML files) |

## Where it is deployed

The site is deployed at **https://legal.suryakumar.us** via
[Cloudflare Pages](https://pages.cloudflare.com/).  Cloudflare Pages
automatically serves files from this repository's root and applies the rules
in `_redirects` and `_headers`.

## How to update the policies

1. Create a new branch from `main`:
   ```bash
   git checkout -b update/policy-description
   ```
2. Edit the relevant HTML file (`privacy.html` and/or `terms.html`).
3. Update the **"Last Updated"** date near the top of the file.
4. Open a Pull Request. Cloudflare Pages will post a **preview deploy URL**
   in the PR comments — use it to review the rendered pages before merging.
5. Once approved, merge into `main`. Cloudflare Pages automatically deploys
   the updated site within a few seconds.

> **Note:** Any substantive change to the policy content (new data practices,
> changed opt-out instructions, updated contact information, etc.) should be
> reviewed by a knowledgeable reviewer before merging, to ensure continued
> Twilio 10DLC compliance.

## Contact

Questions about these policies? Email
[ur2cdanger@gmail.com](mailto:ur2cdanger@gmail.com).
