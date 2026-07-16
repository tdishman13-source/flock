BLACK SHEEP - install as a phone app

1) Host this folder on a free static host:
   - GitHub Pages (what we used for Cinderhold): github.com -> New repository
     (public, boring name) -> "uploading an existing file" -> drag in the
     7 files (skip the zip) -> Commit. Then Settings -> Pages -> Source:
     Deploy from a branch, main, / (root) -> Save. URL after a minute or two:
     https://YOURNAME.github.io/REPONAME/
   - Or Netlify: app.netlify.com/drop -> drag this whole folder in.

2) Text the family the URL and the passcode. On each phone:
   - iPhone: open the link in Safari -> Share -> Add to Home Screen.
   - Android: open in Chrome -> menu -> Add to Home screen.
   The app itself tells them to do this if they open it in a browser.

3) Launch from the sheep icon. Enter the passcode once per phone.
   Works offline after the first launch.

index.html is the entire game. manifest.webmanifest + sw.js + icons make it
installable and offline-capable. To update later: edit index.html, bump the
cache name in sw.js (blacksheep-v1 -> v2), then in the repo use
Add file -> Upload files to replace index.html and sw.js. Installed phones
pick up the new version by their second launch.

Passcode: the PASSCODE constant near the bottom of index.html.
Kill switch if the link escapes: change the passcode and re-upload, or
rename/delete the repo (the old URL dies instantly).
