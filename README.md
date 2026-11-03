# OpenTaiko-Android-Builds
To build APKs via actions (Experimental)

## How releases are made

The [Build Android Release](.github/workflows/build-release.yaml) workflow builds one APK containing:

- the latest release of [OpenTaiko](https://github.com/0auBSQ/OpenTaiko) (Android project included),
- the latest **Open-World Memories** skin from [OpenTaiko-Skins](https://github.com/OpenTaiko/OpenTaiko-Skins),
- every Character and PuchiChara from OpenTaiko-Skins.

Songs are not bundled: the app offers to download the soundtrack on first launch.

To publish a release, bump the version in [package.txt](package.txt) and push to `main`. The
release is tagged with that version and named `OpenTaiko Android Package <version>`; its
description lists the OpenTaiko and skin versions used. If the tag already exists, the run is
skipped.

The workflow can also be started by hand (Actions → Build Android Release → Run workflow), with an
optional OpenTaiko tag, branch or commit to build instead of the latest release.
