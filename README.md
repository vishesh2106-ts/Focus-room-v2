# Focusroom — Minimal PCM Tracker

## Publish on GitHub Pages
1. Extract this ZIP.
2. Upload **the contents** of this folder (not the folder itself) into the root of your GitHub repository, replacing the previous app files.
3. Commit the changes.
4. In Settings → Pages, choose `main` and `/(root)`.
5. Open `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/` in Chrome.
6. Refresh once after deployment. The app registers `./sw.js` and uses relative manifest paths so it works under a GitHub project URL.

## Features
- Local chapter checklist for Physics, Chemistry and Maths (concepts, notes, practice, PYQs, revision)
- Daily tasks
- Focus timer with subject-wise study-time totals
- Study statistics
- Pre-board countdown and daily target settings
- JSON export/import backup
- Optional Study Buddy room broadcasts via Supabase Realtime
- Optional camera preview with explicit permission; preview is local to this device and is **not** streamed to a buddy
- PWA manifest, icons and service worker for installation/offline app shell

## Study Buddy live sync
Solo tracking works without a backend. To sync a room between devices:
1. Create a free Supabase project.
2. In Supabase, enable Realtime for your project.
3. Copy the Project URL and publishable/anon key from Project Settings → API.
4. Paste them in Focusroom → Settings → Supabase connection on both devices.
5. One person creates a room and shares the invite link. The other opens it and connects.
Only use the publishable/anon key. Never put a service-role key in a browser app.

## Notes
- Tasks, chapter progress and study time are stored in this browser's localStorage. Export a backup before clearing browser data or changing devices.
- Browser notifications are not enabled in this starter; foreground buddy status broadcasts display in-app notifications while the app is open.
- Camera is never activated automatically and is not transmitted to another person.
