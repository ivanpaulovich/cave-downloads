# Cave downloads

The public Android download page and release files for Cave. The game's C++
source, signing keys, and private crash symbols are not included here.

This repository is published from `main` with GitHub Pages. Open `index.html`
locally to preview; no dependencies or build step are required.

## Publishing an update

1. Build and verify a signed Release APK using the private game project. Keep
   the same signing key and increase the Android version code.
2. Publish a GitHub Release with `cave-android.apk` and its matching
   `cave-android.apk.sha256` file. Never upload signing keys or private symbols.
3. Update the version, date, size, checksum, and versioned download URLs in
   `index.html`, then push to `main`.

The initial Android release is experimental and still needs testing on phones.
