# Cave downloads

The public download page and release files for Cave across Android, Windows,
and Linux. The game's C++ source, signing keys, and private crash
symbols are not included here.

This repository is published from `main` with GitHub Pages. Open `index.html`
locally to preview; no dependencies or build step are required.

## Publishing an update

1. Build each platform artifact from the private game project and keep only
   artifacts that passed their package verification. Android must use the
   existing release signing key; increase its version code for every update.
2. Publish one GitHub Release with the platform artifacts and matching
   `.sha256` files. Never upload signing keys or private symbols. The desktop
   packages are relocatable archives; keep their executable, resources and
   bundled libraries together.
3. Update the version, date, and versioned download URLs in `index.html`, then
   push to `main` so GitHub Pages publishes the page.

The v0.1.5 Android build requires Android 10+, ARM64, and Vulkan dynamic
rendering. The Windows and Linux packages target x86_64 desktop systems.
macOS is not included in this release. All editions are early builds and the
Android package still needs real-device testing.
