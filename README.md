# ByBroken.github.io (GitHub Pages user site)

Contents for a repo named exactly `ByBroken.github.io` (user site, served at https://bybroken.github.io/).
Only purpose: serve `/.well-known/assetlinks.json` at the domain root so the Colorear Android app
(Trusted Web Activity, package `io.github.bybroken.colorear`) opens full-screen without the browser URL bar.

- `.nojekyll` makes GitHub Pages publish the `.well-known` folder (Jekyll skips dot-folders).
- `index.html` redirects the root to /colorear/.
- After enabling Play App Signing, add the Play Console **app signing key** SHA-256
  (Test and release > App integrity > App signing) as a second entry in `sha256_cert_fingerprints`.
  Keep the upload key fingerprint too (useful for sideloaded test APKs).

Check: https://developers.google.com/digital-asset-links/tools/generator
or: https://digitalassetlinks.googleapis.com/v1/statements:list?source.web.site=https://bybroken.github.io&relation=delegate_permission/common.handle_all_urls
