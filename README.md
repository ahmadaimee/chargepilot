# ChargePilot — public download site

This **public** repo holds only:

- `index.html` + `vercel.json` — the download landing page (deployed by Vercel)
- `ChargePilot-Setup.exe` — the Windows installer

It contains **no source code**. The app's source lives in a separate private repo;
Vercel deploys *this* repo so it never has access to the source.

**Download link** (served raw by GitHub, used by the page + the in-app updater):

    https://raw.githubusercontent.com/ahmadaimee/chargepilot/main/ChargePilot-Setup.exe

`.vercelignore` keeps the .exe out of the Vercel build (the file is downloaded from
GitHub raw, not from the Vercel domain), so deploys stay fast.

To publish a new version: rebuild the installer, overwrite `ChargePilot-Setup.exe`
here, and `git push`. See BUILD.md in the source repo for the full flow.
