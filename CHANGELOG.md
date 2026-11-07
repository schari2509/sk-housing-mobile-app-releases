# Changelog

All notable changes to the Surya Kiran Housing mobile app are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/); versions follow [SemVer](https://semver.org/).

## [1.1.2] - 2026-11-07

### Fixed
- Google sign-in: new users are now taken to the "Complete Your Profile" screen after signing in, on both the login and register screens. Previously they were signed in straight away with placeholder details (wing A1, flat 101, no phone number). This also applies to half-finished accounts and when the server can't be reached. Submitting the form signs you in and opens the dashboard; Cancel signs you out.

## [1.1.1] - 2026-11-07

### Fixed
- Profile: the app version shown in the subtitle and the about dialog was hardcoded (v1.0.0 / 1.0.0+1). It now reads the installed build's real version, so it always matches the app.

## [1.1.0] - 2026-11-07

### Added
- Generate bills: choosing "Specific Flats" now shows a chip for every flat (labelled like "A1-101"). Tap the chips to select which flats to bill.

## [1.0.1] - 2026-11-07

### Changed
- Committee chat: `@mentions` now have a highlighted background. Your own messages show a translucent white highlight; other people's messages show a light tint of the primary colour.

## [1.0.0] - 2026-11-07

### Added
- Initial release.
