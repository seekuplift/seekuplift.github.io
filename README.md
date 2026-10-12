# seekuplift.com

GitHub Pages site for `seekuplift.com`.

- `.well-known/assetlinks.json` — Android App Links + Mobile Wallet Adapter identity for
  `com.seekuplift.app`. The fingerprint is the EAS release keystore's SHA-256. When Google Play
  App Signing is added, append its fingerprint; never remove the dApp Store key's entry.
- `.well-known/security.txt` — RFC 9116 security contact (`security@seekuplift.com`). Renew
  `Expires` before 2027-10-11.
- `.nojekyll` must stay, or Pages drops the `.well-known/` directory.
- DNS is on Cloudflare (proxied). A Cloudflare Response Header Transform Rule sets
  `Content-Type: application/json` on `/.well-known/assetlinks.json`. Phantom's identity check
  (solana-mobile digital-asset-links) rejects GitHub Pages' `application/json; charset=utf-8`,
  so don't remove that rule.
