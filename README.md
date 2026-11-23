# Little Detours

Daily and weekly photo dares, plus family photowalk games, at three levels (Easy, Medium, Hard). Shoot it, frame it, share it.

Little Detours is a small, installable web app (PWA). Each day and week it deals out a fresh set of photo dares. Take the photo, and the app turns it into an instant-style print with the dare written on it in grease pencil. You can keep it or share it.

## Features

- **Today's dares** and **This week's dares**: new prompts at three difficulty levels
- **Family photowalk games** for heading out with kids
- **Your prints**: a gallery of finished dares, stored on your device (IndexedDB / localStorage)
- **Share** prints through the native share sheet where it's supported
- **Works offline** and can be installed to the home screen (service worker + web manifest)
- Light and dark themes

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles and script |
| `sw.js` | Service worker for offline caching |
| `manifest.webmanifest` | PWA manifest (name, colours, icons) |
| `icon-*.png` | App icons |

## Running locally

No build step and no dependencies. Serve the folder over HTTP (service workers don't run from `file://`):

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploying

This is a static site, so any static host will do. For GitHub Pages: **Settings → Pages → Deploy from branch → `main` / root**.

## Privacy

Photos and progress stay in your browser. Nothing is uploaded anywhere.
