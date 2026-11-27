# tracked-out-releases

Public update feed for Tracked Out (spec 019 in MTKRiley/cluade-apps).

- `latest.json`: the newest version, its notes, and the signed Windows update installer's URL and signature. Installed copies of Tracked Out read it on launch and from **Check for updates**.
- `app/<version>/TrackedOut_<version>_update.exe`: the small signed update installer for that version.
- Release `runtime-<v>` (GitHub Releases): the runtime pack `runtime-<v>.tar.gz`. The full installer already carries it; the app downloads it only if its copy is missing.

The app only installs an update signed with the Tracked Out key for the version that `latest.json` names. These files are written by `scripts/release-manifest.sh` in the app repo; don't edit them by hand.
