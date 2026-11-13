# Backbone live feed (staged, NOT published)

`live.json` is the one public file the Backbone app reads (`live.url`). It holds only the last two daily closes of 5 coins, taken from the app's own bundled data (`apps\backbone-demo\data_in`). It has no keys, no private data and no PC paths, and key_scan PASSED on it (13 Nov 2026).

To make it live, do this only after zac types "push it":
1. Publish this folder to a GitHub Pages repo of its own, e.g. `backbone-live`. Don't reuse another project's repo, feed or key.
2. Set `live.url` in `v4.1\MASTER_BACKBONE\apps\backbone-demo\app.json` to `https://<account>.github.io/backbone-live/live.json`.
3. Rebuild the APK with versionCode 6. `live.url` is baked into the APK, so the v2.0 APK won't see it without a rebuild. A rebuild needs less than 1 GB, but C: has only 4.6 GB free.
