# Changelog

## 0.1.1 - 2026-10-04

- Keep the previous completed hour as the stopwatch's full base ring. The next hour's color advances over it; blue, red, green, and purple repeat in order.
- Match the moving rim highlight to the color underneath it instead of recoloring the uncovered base.
- Apply the same completed-hour behavior to mini-window progress and the non-Metal ring fallback.
- Add hour-boundary/color-cycle checks and real GPU rendering tests in both appearances. All 40 tests pass.

Study records, daily totals, calendar behavior, and countdown timing are unchanged. This remains an ad hoc signed Apple silicon preview without Apple notarization or an automatic updater.

## 0.1.0 - 2026-10-02

First public preview for Apple silicon Macs. Source remains private.

- Stopwatch, countdown up to four hours, compact mini window, and configurable daily-goal calendar.
- English and Simplified Chinese, adjustable content size, and native glass controls on macOS 26+.
- Shared daily study totals; new breaks are excluded from learning statistics.
- Optional, system-managed launch at login in Settings. No automatic registration during installation or normal launch.
- Quiet login launch with the timer paused; safe removal of recognized older login-agent files after user choice.
- Versioned, release-optimized app bundle, distributed with ad hoc signing and a SHA-256 checksum.

Known limits: no Developer ID signature or Apple notarization; Apple silicon only; older systems, actual reboot/login, and Gatekeeper behavior on a clean Mac are not fully verified. Old countdown records cannot reliably distinguish breaks, so historical totals remain unchanged. No cloud sync, automatic updater, or dedicated backup/export feature.
