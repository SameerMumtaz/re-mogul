# RE Mogul 🏙️

Build a real estate empire from one property and $30K to $100,000,000.
Seeded with a real Irving, TX deal — 7-Eleven + Kabobs To Go, $1.7M @ 6.75% with rate resets, lease step-ups, and a 2037 tenant-expiry event baked in.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire game — self-contained, no build step |
| `manifest.json` | Add-to-Home-Screen metadata (name, icons, standalone display) |
| `sw.js` | Service worker — caches the shell so the game opens offline |
| `icon-192.png` / `icon-512.png` | App icons (Android/Chrome) |
| `apple-touch-icon.png` | App icon (iOS home screen) |

## Host on GitHub Pages

1. Create a new repo (e.g. `re-mogul`)
2. Upload all 6 files to the repo **root**
3. Repo **Settings → Pages → Source**: select `main` branch, `/ (root)` folder, save
4. Your game goes live at `https://<your-username>.github.io/re-mogul/` within a minute or two

## Add to Home Screen

- **iPhone/iPad:** open the site in Safari → Share → **Add to Home Screen**
- **Android:** open in Chrome → menu (⋮) → **Add to Home screen** / **Install app**

Once added, it launches fullscreen like a native app, works offline, and **your save persists on the device** — progress autosaves after every action to localStorage. The 🔄 NEW GAME button wipes the save and starts fresh.

## Notes

- Saves are per-device/per-browser (localStorage). Clearing site data clears the save.
- All dependencies (React, Tailwind, Babel) load from CDNs — first visit needs internet; after that the service worker serves the cached shell.
