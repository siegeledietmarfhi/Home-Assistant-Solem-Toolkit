# Changelog

All notable changes to this repository will be documented in this file.

## [1.0.4] - 2026-04-21

### Fixed

- Tightened manual station command sequencing for BL-IP controllers by waiting for notifications during the initial subscribe, command write, and commit phases.
- Preferred Home Assistant's Bluetooth registry before direct Bleak scans to improve device resolution with HA-managed adapters and Bluetooth proxies.

### Added

- Added `_reverse_engineering/` notes, test script, and manufacturer reference PDFs so the protocol changes in this fork are documented in-repo.

## [1.0.3] - 2026-04-19

### Changed

- Marked the repository as the maintained fork and updated documentation, ownership metadata, and repository links.
- Refactored Bluetooth/service handling around a dedicated BLE API wrapper.

### Fixed

- Switched manual watering and program control to the verified BL-IP protocol.
- Converted service-level minutes to protocol-level seconds where required.
- Enabled notification subscription before writes so controllers on newer firmware accept manual commands consistently.

## [1.0.2] - 2026-01-13

### Note

- Last upstream release before the maintained fork changes.
- Earlier history is available in Git tags `V1.0.0` through `V1.0.2`.
