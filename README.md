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

`.github/workflows/morphe-root.yml` grabs the latest Morphe CLI and patches (dev channel), picks the newest app version those patches support and patches it.

The stock APK is tried from APKMirror, Uptodown, archive.org, APKPure and Google Play, in that order. Only a full APK signed by Google is used. If the newest supported version isn't up anywhere yet, the build stops instead of falling back to an older one. Google Play needs the `GPLAY_EMAIL` and `GPLAY_AAS_TOKEN` secrets; without them that source is skipped.

SHA-256 checksums are listed in each release's notes.

It runs every day at 19:17 UTC. If nothing changed since the last release it skips the build. You can also start it by hand from the Actions tab and choose the app, patch channel, version, or a direct APK link.
