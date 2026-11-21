# Canvas Grades launcher

A tiny GitHub Pages site that gives the family Canvas Grades web app (a Google Apps Script web app) a proper home-screen icon on Android and iPhone. Apps Script can't add the icon tags phones look for, so this page carries them and forwards to the real app.

## How it works

- `index.html`: the first time you open it on a phone, it asks for the web app link and saves it **in that phone's browser only** (localStorage). The link is never stored in this repo, so the public site doesn't reveal it.
- After that, tapping the home-screen icon opens `./?launch`, which forwards straight to the saved link.
- `manifest.webmanifest` gives Android its icon and name; `icons/apple-touch-icon.png` gives iPhone its icon.

## Setup on a phone

1. Open https://flyingqbert.github.io/canvas-grades-launcher/ (Safari on iPhone, Chrome on Android).
2. Paste the web app link (`https://script.google.com/macros/s/…/exec`) and tap **Save link**.
3. iPhone: Share → **Add to Home Screen**. Android: ⋮ → **Add to Home screen** / **Install app**.

To change the link later, open the site in the browser (not from the icon) and tap **Change saved link**.
