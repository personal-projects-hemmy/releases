# Releases

Downloadable builds of apps made by Philibert Hemmy Ramananjato.

This repository only hosts installers and update files. Source code is not published here.

## Apps

Each app has its own folder with its update feed and notes.

| App | Folder | Platform | Description |
| --- | --- | --- | --- |
| **Focus** (Pomodoro) | [`pomodoro/`](pomodoro) | Windows | A Pomodoro timer with projects, tasks and focus stats. |

## How to install

1. Open the [Releases](../../releases) page.
2. Find the latest release for your app. Release tags are prefixed with the app name, for example `pomodoro-v1.1.0`.
3. Download the installer and run it. Apps with in-app updates check their folder here for new versions automatically.

## Layout

```
<app>/
  README.md     notes and changelog for the app
  latest.yml    update feed read by the app (Windows)
```

Installers are attached to GitHub Releases (tag `<app>-v<version>`), not committed to the repo, because Git blocks files over 100 MB.

## License

Free for **personal, non-commercial use**. See [LICENSE](LICENSE) for the full terms.

For commercial use or redistribution, please contact the author first.
