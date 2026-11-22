# Install ClipSense

Requires macOS 27 or later on Apple silicon. ClipSense is a menu-bar app with no Dock icon.

## 1. Download and verify

Download [ClipSense-0.2.0.dmg](https://github.com/zyvorai/clipsense/releases/download/v0.2.0/ClipSense-0.2.0.dmg) and its `.sha256` file from the [release page](https://github.com/zyvorai/clipsense/releases/tag/v0.2.0). The DMG is Developer ID signed and notarized by Apple.

```
shasum -a 256 -c ClipSense-0.2.0.dmg.sha256
xcrun stapler validate ClipSense-0.2.0.dmg
```

SHA-256 of this release: `9e7fcf271e334ab4699e8ccc806ca9d805099927c0db25fd7c970c1c5fee3980`.

## 2. Install

Open the DMG, drag **ClipSense** to Applications and open it. A Welcome window explains what is read and the macOS pasteboard prompt before anything happens.

## 3. Trial key

You do not need a key. 30-day trial key: [sales@zyvor.dev](mailto:sales@zyvor.dev?subject=ClipSense%20trial%20key). Enter it under **Licence…**. See [LICENSING.md](LICENSING.md).

## Uninstall

Quit ClipSense and delete it from Applications. The encrypted history is `~/Library/Application Support/ClipSense/history.bin`; the key is the Keychain item `dev.zyvor.clipsense.history-key`. Delete both to erase everything.
