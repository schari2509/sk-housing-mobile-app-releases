# Changelog

All notable changes to the Surya Kiran Housing mobile app are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/); versions follow [SemVer](https://semver.org/).

## [1.2.0] - 2026-11-11

### Added
- Add amenities: committee members and admins can add amenities (name, description, rules) from the Amenities screen.
- Edit and delete bills: committee members and admins get Edit (line items and due date) and Delete on every maintenance bill.
- Undo bill generation: after generating monthly bills, a 6-second UNDO option appears before anything is saved to the server.
- Multiple flats: Profile → "Add another flat" links extra flats to your account using wing and flat-number dropdowns, and each extra flat can be removed. Bills for those flats show up under your account.
- Receipt review notifications: committee members are notified when a resident uploads a payment receipt that needs approval.

### Fixed
- Receipt approval not saving: approving a receipt now saves to the database, so the bill no longer goes back to "Under review" after a refresh. If the save fails, the app no longer shows the bill as paid.
- Bill order: maintenance bills now sort in the same flat order as the residents directory.
- Resident count: a person who owns several flats is counted once.

### Internal
- Test suite: repaired so all 83 tests pass, and the 5 that were failing no longer depend on a live backend.

### Release Notes
- Deploy order: deploy the society-sync backend to Vercel before releasing the app. The edit-bill, link-flat and receipt-notification features need the new server code. Receipt approval also needs it, because the fix is on the server.
- Old approvals: bills you already approved still show "Under review" in the database. Approve them again once the backend is live.
- Firestore rules: no changes made.

## [1.1.3] - 2026-11-07

### Fixed
- Google sign-in: new users are no longer saved to the database with a placeholder profile (wing A, flat 101). Nothing is stored and no flat is assigned until you submit the "Complete Your Profile" form with the flat you picked.
- Complete Your Profile: if saving your details fails, you now see an error and stay on the screen. Previously the app silently let you in with a local-only account that never reached the database.

### Changed
- Complete Your Profile: the flat field is now a dropdown of the real flats in the selected wing. Changing the wing clears the flat, and you can't submit without choosing one.

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
