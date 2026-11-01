UNIVERSAL INVENTORY & LOCAL POS SYSTEM - INSTALLABLE PWA

PACKAGE CONTENTS
- index.html: your current app, with service-worker registration added
- manifest.webmanifest: install name, display mode, theme and icons
- sw.js: app-shell and resource caching for repeat/offline launches
- icons/: Android/desktop and Apple touch icons

HOW TO INSTALL
1. Upload the ENTIRE folder contents to a web host that serves HTTPS.
   Keep index.html, manifest.webmanifest, sw.js, and the icons folder together.
2. Open the HTTPS URL in Chrome or Edge.
3. Use the browser's Install app option (or Add to Home Screen on supported mobile browsers).

LOCAL TESTING
- Service workers do not work from a file:// URL.
- For local testing, serve this folder from http://localhost using a local web server.

IMPORTANT NOTES
- The app's inventory data remains in the browser's IndexedDB/local storage on that device.
  Installing the PWA does not automatically sync data between devices.
- Camera access requires HTTPS (or localhost) and browser camera permission.
- The app uses Tailwind CSS and Google Fonts from CDNs. The service worker caches successful
  resource responses after they have been loaded online, but first launch requires internet.
- This package makes the page installable; it does not create a hosted public URL.

LOGIN RECOVERY UPDATE
This build uses IndexedDB schema version 6 and a fresh service-worker cache. Before updating, close every open tab/window of the POS app so the database upgrade can complete. Then reload the hosted HTTPS app. The upgrade preserves existing inventory and sales stores.
