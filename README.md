# NeuroWheel+

An enhanced fork of [neurowheel](https://github.com/Dai1964/neurowheel) — a single-file task wheel designed to cut down decision fatigue: instead of facing a full to-do list, you see 8 tasks at a time and can let the wheel pick one for you.

The original stays untouched and simple. This version adds:

- **Spin** — the centre button spins the wheel and picks a random task for you, instead of just showing you options to choose between.
- **Energy filter** — show only Low / Medium / High energy tasks depending on how much you've got today.
- **Streaks & stats** (📊) — current streak, all-time total, and a 7-day bar chart.
- **Reminders** (⏰) — optional in-app/browser nudges at set times.
- **Backup & restore** — export/import your tasks and history as a JSON file.
- **Installable** — a manifest + service worker let you add it to your home screen and use it offline once loaded (works when served over http/https; opening the file directly still works for everything except install/offline).
- **Accessibility** — category icons (not just colour), keyboard navigation on the wheel, and reduced-motion support.
- **Fixes** — the task timer now survives closing the detail popup, "Done" has an Undo, and long task names get an ellipsis instead of silently clipping.

Open `index.html` in a browser to use it — no build step, no server required.

## iOS

Works fine in Safari on iPhone/iPad, and "Add to Home Screen" installs it as a standalone app icon (using `apple-touch-icon.png`, since iOS doesn't support SVG manifest icons for that). One real gap: iOS only supports web notifications for a site added to the Home Screen, and only from iOS 16.4+ — reminders won't fire in a regular Safari tab, and even installed, they only work while the app is actually open in the foreground (iOS suspends background tabs aggressively). Everything else — the wheel, spin, timer, stats, backup/restore — works the same as on desktop/Android.