# seekuplift.com

GitHub Pages site for `seekuplift.com`.

- `.well-known/assetlinks.json` — Android App Links + Mobile Wallet Adapter identity for
  `com.seekuplift.app`. The fingerprint is the EAS release keystore's SHA-256. When Google Play
  App Signing is added, append its fingerprint; never remove the dApp Store key's entry.
- `.nojekyll` must stay, or Pages drops the `.well-known/` directory.
