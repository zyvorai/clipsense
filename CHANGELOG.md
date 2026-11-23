# Changelog

## v0.3.0 - 2026-11-23

Requires macOS 27 or later, Apple silicon.

- **Nine more things recognised, each with an action:** tracking links (Clean link), Base64 (Decode), Unix timestamps (Convert time), JSON (Minify), terminal colour codes (Strip), CSV/TSV (Markdown table), e-mail and IP addresses (Mask), percent-encoded text (Decode %XX), colour values (Convert colour).
- **Undo** for every action: the original clip goes back on the clipboard.
- **Opt-in automatic tidy-up** (off by default): clean tracking links and strip terminal colours as you copy. Secrets are never changed automatically.
- The first action is highlighted and runs on Return; every action has its own Shift-Command shortcut in History; right-click a clip for its actions; Control-Option-Command-H opens History from anywhere; Command-1 to 5 copy the recent clips again.
- Opening ClipSense shows the History window, opening it again brings History forward, and it has a Dock icon while a window is open (a login launch stays in the menu bar).
- New dark app icon.
- **Fix:** ClipSense could hang at launch, with no menu-bar icon and no window, when the Keychain was locked or waiting for an answer. History now loads in the background and the app says so if the Keychain is slow.

## v0.2.0 - 2026-11-20

First public release (trial). Requires macOS 27 or later, Apple silicon.

- Recognises stack traces, JSON, kubeconfigs, secrets and JWTs; redact, pretty-print, decode and open in cluster context.
- macOS 27 design: Liquid Glass menu-bar popover, History window, Settings, Welcome.
- AES-256-GCM encrypted history with the key in the Keychain; no network entitlement; concealed clips never read.
- Soft licence: never disables a feature. Free 30-day trial key: sales@zyvor.dev.
