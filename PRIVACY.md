# Privacy

## Local Data

StudyTimer saves session identifiers, timer modes and context, start/end timestamps, elapsed duration, and timer/window preferences. Its main history file is:

```text
~/Library/Application Support/StudyTimer/sessions.json
```

Language and the daily goal are stored with macOS UserDefaults. Demo images in this repository use synthetic values; they do not contain the developer's real study history.

New records distinguish stopwatch, study countdown, and break context; breaks do not contribute to study totals. Older records lack context and remain readable. They are not reclassified or deleted automatically, so historical totals may still contain breaks recorded by earlier versions.

## Network and Permissions

The current app source has no network requests, accounts, analytics, advertising, cloud sync, or automatic updater. It uses ordinary macOS window, workspace lifecycle, and graphics APIs. It does not need access to the clipboard, camera, microphone, contacts, or location to time a session.

GitHub hosts this repository, not your running app's study history. GitHub's own account and repository services are separate from the application.

## Storage Limits

History is stored as local JSON, not independently encrypted. Normal filesystem access and any system backups can include it. The app has no dedicated backup, import/export, or secure-deletion feature yet. Do not treat it as a protected record of sensitive activity.

To remove local history, first quit StudyTimer normally, then remove its Application Support folder. This is irreversible unless you have an external backup. Removing the app bundle alone does not remove history or preferences.

## Launch at Login

New installations leave launch at login off. Neither installation nor normal launch adds a login item. Enable it explicitly in Settings after moving the app to Applications; Apple's SMAppService registers the main app with macOS. The switch shows when system approval is still needed. Login launch stays quiet and does not begin a timer.

An existing older StudyTimer login-agent file remains visible through the switch until you change it. Switching off removes the recognized old file and unregisters the modern item; switching on replaces the old file after the modern registration is accepted. The app never removes unrelated login items. Turn this option off before uninstalling the app.

## Reporting Issues

Do not attach real `sessions.json`, full private paths, or personal calendar screenshots to an issue. Use a small synthetic example and describe the timer state, macOS version, and steps that caused the problem.
