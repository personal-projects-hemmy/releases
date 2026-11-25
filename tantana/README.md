# Tantana

A personal money app for Android, in ariary, in English and French.

## Download

Get the latest APK from the [Releases](../../../releases) page: look for tags starting with `tantana-v`, then download `tantana-<version>.apk` on your Android phone and open it.

Android may ask you to allow installs from your browser (or from Tantana, for in-app updates) the first time.

## In-app updates

The app checks this folder for `latest.yml` a moment after it opens, and from **Menu > Check for a new APK**. It is skipped in Expo Go.

- Update feed URL:
  `https://raw.githubusercontent.com/personal-projects-hemmy/releases/main/tantana`
- `latest.yml` is committed here for each new version. The app compares its `versionCode` with the installed one. When it is higher, the app offers to download the APK from `url` (the asset attached to the matching GitHub Release), checks its checksum, and opens the Android installer. For example:
  `https://github.com/personal-projects-hemmy/releases/releases/download/tantana-v1.0.5/tantana-1.0.5.apk`
- Every APK is signed with the same key, so it installs over the previous version and keeps the app's data.

## Publishing a new version

1. Bump `expo.version` and `expo.android.versionCode` in the app's `app.json`.
2. Build locally: `npx expo prebuild -p android --clean`, then `./gradlew assembleRelease` in `android/`, and sign the APK with the app's release key (`zipalign` + `apksigner`).
3. Create a GitHub Release here tagged `tantana-v<version>` and attach `tantana-<version>.apk`.
4. Update `latest.yml` in this folder: `version`, `versionCode`, `url`/`path` to that release asset, `sha512`, `sha256`, `md5`, `size`, `releaseDate`, `notes` and `notesFr`. Commit it last, after the asset is uploaded.

## Changelog

- **1.0.6** (build 7) - dark mode with a System / Light / Dark setting synced across devices.
- **1.0.5** (build 6) - fingerprint lock, email sign in / register / forgot password, delete account, already-registered email check, and in-app updates from this page. First build made outside EAS.

## License

Personal, non-commercial use only. See [LICENSE](../LICENSE).
