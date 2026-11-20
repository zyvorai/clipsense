# FAQ

**Does ClipSense send anything over the network?**

No. It ships with an empty entitlements file and the hardened runtime: no network client entitlement. Check it yourself with codesign -d --entitlements - /Applications/ClipSense.app. Note that it is not sandboxed.

**Does it read my password manager?**

No. Clips marked concealed, transient or auto-generated, clips from known password-manager types, and copies made while a known password manager was in front are skipped and only counted, never stored.

**How is history stored?**

One AES-256-GCM encrypted file in Application Support. The key is random and lives only in your login Keychain. If the Keychain refuses, history stays in memory; there is no plaintext fallback. Clips over 256 KB are not recorded.

**Will macOS ask about pasteboard access?**

It may. macOS can show “Allow paste from other apps” the first time an app reads the pasteboard without a paste. The Welcome window explains it first. If you deny it, ClipSense stops reading and says so; nothing is switched off by licensing.

**Is there a free trial?**

Yes: a free 30-day trial key from sales@zyvor.dev. Without a key everything still works.

**What happens without a key, or when a trial ends?**

Nothing is disabled. A status line shows where your licence stands.

**How much does it cost?**

Pricing is coming. For now it is trial only; write to sales@zyvor.dev if you want to be told when licences open.

**Are the screenshots real?**

They are the real app windows rendered with invented sample data and fake secrets, not captures of anyone's clipboard.

**Which macOS versions?**

macOS 27 or later, Apple silicon.
