# Privacy

- **No network.** ClipSense ships with an empty entitlements file and the hardened runtime. There is no `com.apple.security.network.client`. It is **not** sandboxed. Verify:

```
codesign -d --entitlements - /Applications/ClipSense.app
```

- **Concealed and transient clips are never read.** The pasteboard's type list is checked first; clips marked concealed, transient or auto-generated, clips with password-manager types, and copies made while a known password manager was in front are skipped and counted, never stored.
- **History is encrypted.** AES-256-GCM, file `~/Library/Application Support/ClipSense/history.bin` (mode 0600). The 256-bit key is random and lives in your login Keychain, this device only. If the Keychain refuses, history stays in memory; there is no plaintext fallback.
- **Secrets are masked** and, by default, never written to disk. Clips over 256 KB are not recorded.
- **Open in Cluster Context** works on a private 0600 copy of the kubeconfig and removes it when the shell exits. Your own `~/.kube/config` is not touched.
- **Pasteboard prompt.** macOS may ask "Allow paste from other apps" the first time ClipSense reads the pasteboard. If access is denied ClipSense does not read it and says so.
- JWT decoding never verifies the signature.
