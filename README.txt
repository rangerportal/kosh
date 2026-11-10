KOSH MONEY BOOK — installable offline PWA

HOW TO PUT IT ON YOUR PHONE
A PWA must be served over https once, then it works fully offline.
Easiest free options:
  • Netlify Drop: open app.netlify.com/drop and drag this whole folder in.
  • GitHub Pages: push these files to a repo, enable Pages.
Then open the link in Chrome (Android) → menu → "Install app" / "Add to Home screen".
On iPhone: open in Safari → Share → "Add to Home Screen".

FILES
  index.html            the whole app (UI, logic, storage)
  manifest.json         app name, icons, standalone display
  sw.js                 service worker: caches the app for offline use
  icon-*.png            home-screen icons

DATA & SECURITY
  • Accounts and entries are stored in this phone's IndexedDB. Nothing is uploaded.
  • Passwords are hashed with PBKDF2-SHA256 (150,000 rounds, random salt).
  • Mobile number is validated (Indian 10-digit) and must be unique; no SMS OTP,
    because an offline app has no server to send one.
  • Back up from Profile → "Back up data" before clearing browser data or switching phones.
