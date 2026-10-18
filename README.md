# ATELIER — Digital Closet

A local-first, installable Progressive Web App for your wardrobe.

## Included features
- Add clothing photos from the camera or photo library
- Store item photos and metadata locally in the browser (IndexedDB)
- Category and text search
- Outfit combinations based on items you own, occasion, weather selection, and style tags
- Save favorite outfits
- Weekly outfit planner
- Log wears and estimate cost per wear
- Basic shopping suggestions based on missing/low-count categories
- JSON export/import backup
- Offline app shell via service worker

## Important implementation notes
- Outfit generation is a local rules-based stylist, not a hosted generative AI model. It requires no API key and does not upload closet data.
- Weather is selected manually in this version; it does not fetch live weather.
- Data is stored in the browser's IndexedDB and localStorage on this device/browser profile. It is not automatically synced to another device. Clearing site data can delete the closet, so export backups regularly.
- The app is a PWA, not an App Store native app.

## Put it on your iPhone Home Screen
1. Upload these files to a static HTTPS host (GitHub Pages is one free option; Netlify or Cloudflare Pages are alternatives).
2. Open the published HTTPS URL in Safari on your iPhone.
3. Tap Share → Add to Home Screen. If shown, enable “Open as Web App”, then tap Add.
4. Open the new ATELIER icon from your Home Screen. Add a test item and export a backup before importing a large wardrobe.

For GitHub Pages: create a repository, upload `index.html`, `manifest.json`, `sw.js`, and `icon.svg` to the repository root, then enable Pages in repository Settings. Wait for the HTTPS site URL, open it in Safari, and add it to the Home Screen. Exact GitHub UI labels may change.

## Local testing
Serve the directory over HTTP(S) (service workers do not run from `file://`). IndexedDB works in Safari when opened as a site.
