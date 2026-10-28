LOCAL MUSIC IPOD — PWA PACKAGE

Files:
- index.html: the iPod app
- manifest.webmanifest: installable app details
- sw.js: app-shell offline cache
- icons/: app icons

IMPORTANT: To install as a PWA, serve this folder from HTTPS (or localhost). Opening index.html directly as file:// will not enable service workers or installation.

Easiest hosting:
1. Upload the contents of this folder to a static HTTPS host, such as GitHub Pages or Netlify.
2. Open the hosted index.html URL on your phone.
3. Android/Chrome: use the browser menu and choose Install app / Add to Home screen.
4. iPhone/iPad: open the URL in Safari, tap Share, then Add to Home Screen.
5. Launch from the home-screen icon once online so the service worker can cache the app shell. After that, the app shell can launch offline.

Music remains in each browser/device's IndexedDB. It does not automatically sync between devices. Export a library backup from the in-app menu before clearing browser data or changing devices. Large backup JSON files contain the audio and can be very large.

PWA limitations:
- Browser storage can be cleared or evicted by the OS; keep backups.
- iOS PWA storage and background playback have platform-specific limitations.
- This package is a static PWA, not a signed native App Store / Google Play application.
