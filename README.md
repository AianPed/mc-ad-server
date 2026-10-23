# mc-ad-server

Static advertising manifest for MC Coding & Macro and future Windows utilities.

## Deployment
- Host the repository as a static site on Cloudflare Pages.
- No framework; build command: `exit 0` (or blank, if supported); output directory: `.` (repository root).
- Production branch: `main`.
- Confirm that `https://YOUR-ACTUAL-PAGES-DOMAIN/ads/ads.json` returns JSON.
- **Do not hardcode a guessed `pages.dev` hostname.** Copy the production URL from the deployed Cloudflare project.

## Advertising manifest
- `/ads/ads.json` always contains `version`, `updated`, and `ads`.
- `ads: []` means no paid advertisements; the Windows app displays its bundled default banner.
- Add actual image files under `ads/` only when ready to publish ads.

## Security
- All static site content is public. Do not place secrets, tokens, credentials, advertiser private data, or payment records in this repository.
- Do not put a GitHub personal access token into a public admin HTML page.
