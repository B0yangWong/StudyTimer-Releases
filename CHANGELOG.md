# Changelog

## 0.1.0 - 2026-10-02

First public preview for Apple silicon Macs. Source remains private.

- Stopwatch, countdown up to four hours, compact mini window, and configurable daily-goal calendar.
- English and Simplified Chinese, adjustable content size, and native glass controls on macOS 26+.
- Shared daily study totals; new breaks are excluded from learning statistics.
- Optional, system-managed launch at login in Settings. No automatic registration during installation or normal launch.
- Quiet login launch with the timer paused; safe removal of recognized older login-agent files after user choice.
- Versioned, release-optimized app bundle, distributed with ad hoc signing and a SHA-256 checksum.

Known limits: no Developer ID signature or Apple notarization; Apple silicon only; older systems, actual reboot/login, and Gatekeeper behavior on a clean Mac are not fully verified. Old countdown records cannot reliably distinguish breaks, so historical totals remain unchanged. No cloud sync, automatic updater, or dedicated backup/export feature.
