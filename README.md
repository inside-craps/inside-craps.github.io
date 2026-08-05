# inside-craps.github.io

Public web presence for **Inside Craps** and the **Chip Rack** app.
Served by GitHub Pages from `main` / root at <https://inside-craps.github.io/>.

Plain static HTML. No build step, no dependencies, no external requests — the pages
deliberately load no fonts, scripts or assets from third parties.

| file | purpose |
|---|---|
| `index.html` | Landing page |
| `privacy.html` | **Privacy policy — see the warning below** |
| `.nojekyll` | Skips the Jekyll build; Pages serves the files as-is |

## ⚠️ Do not rename or move `privacy.html`

`https://inside-craps.github.io/privacy.html` is submitted as the privacy policy URL in **both**
the Google Play and App Store listings, and both stores require a live, reachable policy as a
condition of publication.

Renaming the file, moving it into a subdirectory, or restructuring the site breaks that URL and
puts both listings out of compliance — silently, since nothing warns you. If it ever has to move,
update the URL in both store consoles **first**.

## Editing the privacy policy

The policy must keep matching the app's actual behaviour, and it is also cross-checked against
the Play **Data Safety** declaration. As of the current release, Chip Rack:

- stores all user data locally on device; no accounts, no server, no sync
- contacts one remote service only — the Expo update service, sending just the runtime version,
  release channel and platform. No device identifier, no user identifier, none of the user's data
- runs no analytics, telemetry, crash reporting, advertising or tracking

If any of that changes, update this policy **before** the change ships, bump the effective date,
and re-check the Data Safety answers in Play Console so the two documents agree.

## Why this repo is separate from the app

The app lives in `inside-craps/chip-rack`, which is **private**. GitHub Pages from a private repo
requires a paid plan, so the public site is split out here.

⚠️ **This repo is public.** Never commit credentials, service account keys, `.env` files, signing
material, or anything else that belongs in the private repo.

## Publishing

Pushing to `main` deploys. If the site isn't live, check **Settings → Pages** and confirm the
source is set to deploy from `main` / `/ (root)`.

---

© 2026 Inside Craps. All rights reserved. Not open-source software; no license is granted for
reuse of this content.
