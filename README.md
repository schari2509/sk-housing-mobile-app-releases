# Surya Kiran Housing — Mobile App Releases

This repository hosts the **Android APK releases** for the Surya Kiran Housing Society mobile app, a cross-platform Flutter app for residents and managing committee members.

Source code lives in a separate repository (`SKR/mobile_app`). This repo only distributes builds.

## Latest release

| Version | Date | Download |
|---------|------|----------|
| 1.2.0 (build 7) | 2026-11-11 | See [Releases](../../releases/latest) |

See [CHANGELOG.md](CHANGELOG.md) for the full history.

## Installing

1. Download the latest `.apk` from the [Releases](../../releases) page onto your Android device.
2. Open the file. If prompted, allow installs from this source (Settings → Security → Install unknown apps).
3. Tap **Install**.

To update, install the newer APK over the existing one. Your data is kept as long as the app is signed with the same key.

## About the app

- Dashboard with dues, complaints, events and notices
- Flats and residents directory
- Managing committee contacts
- Notices and announcements
- Bills, complaints, visitors and events

## Releasing a new version

1. Build the APK in the source repo: `flutter build apk --release`.
2. Rename it to `sk-housing-vX.Y.Z.apk`.
3. Add an entry at the top of [CHANGELOG.md](CHANGELOG.md).
4. Update the "Latest release" table above.
5. Commit, tag (`git tag vX.Y.Z`), push, and create a GitHub Release with the APK attached.

Versions follow [Semantic Versioning](https://semver.org/) and match `version:` in the app's `pubspec.yaml`.
