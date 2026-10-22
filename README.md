# LOST HALIDE — Empty Wireframe + Local Upload Prototype

This is a clean, responsive skeleton for a photography portfolio. It does not include third-party photographs. The image areas remain empty until you upload your own work.

## Files
- `index.html`: public-facing wireframe
- `admin.html`: upload/manage prototype
- `styles.css`: responsive desktop/mobile layout
- `app.js`: image preview, local save, listing, and delete

## Test
Open `index.html` and `admin.html` using a local static server or deploy the files to a static host. For example, from this folder run `python -m http.server 8000` and visit `http://localhost:8000`.

## Upload from computer or phone
Open `admin.html`, tap/click the image selection area, choose one or more images, add details, and press save. The file input uses `accept="image/*"` so it works with desktop file pickers and mobile photo pickers (the exact picker depends on the device/browser).

## Important prototype limitation
This prototype stores image data in IndexedDB on the current browser/device. It is useful for checking the layout and upload flow, but it does **not** upload images to a server, sync between your phone and computer, or publish newly uploaded images for other visitors. Browser storage may be cleared, and large image files are limited to 8 MB each in this prototype.

For a real public admin system, connect an authentication service, online database, and image storage provider (for example Firebase Authentication + Firestore + Cloud Storage). Do not treat a hidden admin link as security. A static website alone cannot securely accept shared uploads.
