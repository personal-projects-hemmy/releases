# Focus (Pomodoro)

A Pomodoro timer for Windows with projects, tasks and focus stats.

## Download

Get the latest installer from the [Releases](../../../releases) page: look for tags starting with `pomodoro-v`, then download `pomodoro-<version>-setup.exe`.

## In-app updates

The app checks this folder for `latest.yml` on startup and from **Settings > Check for updates**.

- Update feed URL (electron-builder `generic` provider):
  `https://raw.githubusercontent.com/personal-projects-hemmy/releases/main/pomodoro`
- `latest.yml` is committed here for each new version. Its `path`/`url` points to the installer attached to the matching GitHub Release, for example:
  `https://github.com/personal-projects-hemmy/releases/releases/download/pomodoro-v1.1.0/pomodoro-1.1.0-setup.exe`

## Publishing a new version

1. Bump `version` in the app's `package.json` and build with `electron-builder --win`.
2. Create a GitHub Release here tagged `pomodoro-v<version>` and attach the `.exe` and `.exe.blockmap`.
3. Commit the generated `latest.yml` to this folder, with the installer URL set to that release asset.

## Changelog

- **1.0.0** - first version.

## License

Personal, non-commercial use only. See [LICENSE](../LICENSE).
