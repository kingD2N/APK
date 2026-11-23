# APK

YouTube and YouTube Music patched with [Morphe](https://github.com/MorpheApp), built for rooted devices. No MicroG needed.

Grab the APKs from [Releases](../../releases/latest).

## What you get

- **YouTube** and **YouTube Music**, arm64-v8a only, in one release
- `GmsCore support` and `Custom branding` are left out, so the package name, icon and app name stay stock
- Settings entry shows up as **Morphe (Patch By kingD2N)**
- The APKs keep Google's original signature, so your account stays signed in across updates

## Installing

Signature verification has to be off on the device (CorePatch or similar). Then install the APK over the stock app like a normal update.

## Builds

`.github/workflows/morphe-root.yml` grabs the latest Morphe CLI and patches (dev channel), picks the newest app version those patches support, pulls the stock APK from APKPure and patches it.

It runs every day at 19:17 UTC. If nothing changed since the last release it skips the build. You can also start it by hand from the Actions tab and choose the app, patch channel, version, or a direct APK link.
