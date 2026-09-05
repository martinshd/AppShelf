[中文](usage.md) | **English**

# AppShelf User Guide

## Installing the preview build

The current version is a free preview build that is not notarized by Apple. Only an Apple silicon (M-series) build is provided, requiring macOS 14 or later.

1. Download `AppShelf-<version>.dmg` from [Releases](https://github.com/martinshd/AppShelf/releases).
2. Double-click the DMG and drag `AppShelf.app` to your Applications folder.
3. On first launch, if macOS says the developer cannot be verified, proceed only if you trust the source and want to try the preview: in Applications, Control-click the AppShelf icon and choose Open, then confirm in the dialog; or go to System Settings → Privacy & Security and choose "Open Anyway". See [Apple's guide](https://support.apple.com/en-us/102445).
4. If macOS reports the app is damaged or malware, stop, verify the SHA-256 checksum of your download against `SHA256SUMS.txt` attached to the release, and open an Issue if it still doesn't match.

To verify the checksum (in Terminal):

```bash
shasum -a 256 ~/Downloads/AppShelf-<version>.dmg
```

Compare the output with `SHA256SUMS.txt` in the release. A match means the file is intact.

## Interface layout

- Left sidebar: "All Apps", "Pinned", and the groups you create.
- Right grid: the currently selected collection. In the "All Apps" view, pinned apps stay in a fixed section above the grid.
- Search field at the top: matches application names only.
- "Refresh Apps" in the toolbar: rescans the application folders.
- The interface follows your system language (Chinese and English supported).

![Interface overview (apps shown are fictional)](images/en/overview.png)

## Common actions

| Action | How |
| --- | --- |
| Open an app | Click its icon |
| Pin / unpin | Right-click the app icon and choose Pin / Unpin |
| Reorder pinned apps | Drag icons in the pinned section or the "Pinned" view |
| Create a group | Click the + button next to "My Groups" in the sidebar |
| Add to a group | Right-click the app icon and choose the target group from "Add to Group" |
| Delete a group | Right-click the group name in the sidebar and choose "Delete Group" |
| Show in Finder | Right-click the app icon and choose "Show in Finder" |
| Show / hide the window | Press `Option + Space` |

## Data and privacy

- Pinned apps and groups are stored locally on your Mac; nothing is uploaded.
- The app only reads system application folders (`/Applications`, `/System/Applications` and the built-in system app folder, plus `~/Applications`) to obtain app names and icons.
- The app contains no analytics or telemetry.

## Known limitations

- Apple silicon Macs only; no Intel build yet.
- Not notarized by Apple; first launch requires the confirmation steps above.
- Search matches application names only — no pinyin, abbreviations, or file search.

## Feedback

Please open an [Issue](https://github.com/martinshd/AppShelf/issues) with your macOS version, AppShelf version, and steps to reproduce.
