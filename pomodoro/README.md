# Focus (Pomodoro)

A Pomodoro timer for Windows with projects, tasks and focus stats.

## Download

Get the latest installer from the [Releases](../../../releases) page: look for tags starting with `pomodoro-v`, then download `pomodoro-<version>-setup.exe`.

## In-app updates

The app checks this folder for `latest.yml` a few seconds after it opens, and from **Settings > Updates** (gear icon at the bottom of the sidebar; 1.1.0 used a separate Updates icon).

- Update feed URL (electron-builder `generic` provider):
  `https://raw.githubusercontent.com/personal-projects-hemmy/releases/main/pomodoro`
- `latest.yml` is committed here for each new version. Its `path`/`url` points to the installer attached to the matching GitHub Release, for example:
  `https://github.com/personal-projects-hemmy/releases/releases/download/pomodoro-v1.1.0/pomodoro-1.1.0-setup.exe`

## Publishing a new version

1. Bump `version` in the app's `package.json` and build with `electron-builder --win`.
2. Create a GitHub Release here tagged `pomodoro-v<version>` and attach the `.exe` and `.exe.blockmap`.
3. Commit the generated `latest.yml` to this folder, with the installer URL set to that release asset.

## Changelog

- **1.1.1** - New Settings (gear icon in the sidebar) with Display mode: Auto (follows Windows), Light or Dark. Updates moved into Settings, with a red dot on the gear when an update is waiting.
- **1.1.0** - Check for updates inside the app (Updates icon in the sidebar). From this version on, updates download and install from the app. Users on 1.0.0 need to install 1.1.0 manually once.
- **1.0.0** - first version.

## License

Personal, non-commercial use only. See [LICENSE](../LICENSE).
