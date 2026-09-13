# Nokia Snake — Reimagined

A premium, modern rebuild of the classic Nokia Snake game: full-screen touch
controls, smooth interpolated motion, glassmorphism UI, and 50 levels with
rising speed and obstacles.

## Files you need in your GitHub repo

Create these exact files with these exact paths (GitHub's "Add file → Create
new file" lets you type a full path like `www/index.html` as the filename —
it will create the folders automatically):

```
config.xml
package.json
www/index.html
.github/workflows/build-apk.yml
```

## How the APK gets built

1. Push these files to the `main` branch of your repo (or click **Run workflow**
   manually from the **Actions** tab).
2. Go to the **Actions** tab of your repo. You'll see a run called
   **Build APK** in progress. It takes 3–6 minutes.
3. When it finishes with a green check, open that run and scroll to
   **Artifacts** at the bottom.
4. Download **nokia-snake-debug-apk** — it's a `.zip` containing the `.apk`.
5. Unzip it on your phone (or transfer it there), then tap the `.apk` file
   to install.
6. Your phone will warn about "installing from unknown sources" — allow it
   for this file. This is normal for any APK not from the Play Store.

## Notes

- This is a **debug build** — perfect for testing on your own device. It's
  not signed for the Play Store, but installs and runs identically.
- The game itself lives entirely in `www/index.html` — a single
  self-contained file (game logic, styling, and UI). If you want to change
  colors, level count, or difficulty curve, that's the only file to edit.
- `config.xml` controls the Android app shell: full-screen mode, portrait
  lock, status bar styling, and the app ID (`com.nokia.snake.reimagined`).
- If you rename the app or the package ID, update `config.xml`'s
  `<widget id="...">` and `<name>` fields.
