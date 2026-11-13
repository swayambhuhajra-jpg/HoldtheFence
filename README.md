# Hold the Fence – Android build

GitHub builds the APK automatically. You don't need to install anything on your computer.

| File | What it is |
|---|---|
| `index.html` | The game. Replace this file to update the game. |
| `HoldTheFence-Android.zip` | The Android project (Capacitor 8). App ID `com.xcubelabs.holdthefence`. |
| `.github/workflows/build-apk.yml` | The build instructions GitHub follows. |
| `docs/GAME_NOTES.md` | Game design notes and the dated change log. |
| `docs/upgrades.csv` | Upgrade values waiting for approval. |

## Get the APK (direct download, no unzipping)
1. Open the **Actions** tab and wait for the newest run to show a green tick. This takes about 5–8 minutes.
2. Open **Releases** on the right side of the repo's main page, or go to `/releases/latest`.
3. Tap `HoldTheFence-debug.apk`. On a phone it downloads as an APK you can install straight away.

The same build is also under **Actions**, then the run, then **Artifacts**. That copy comes zipped.

## Update the game
1. Click `index.html`, then the pencil menu, then **Upload files**.
2. Drop the new `index.html` and press **Commit**.

A new build starts by itself.

## Rebuild without changes
Go to **Actions**, open **Build Hold the Fence APK**, and press **Run workflow**.

## Play Store build (optional)
Add these secrets under **Settings → Secrets and variables → Actions**: `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS` and `KEY_PASSWORD`.
Each build then also produces `HoldTheFence-release.aab` for Play Console.
