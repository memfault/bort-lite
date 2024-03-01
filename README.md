# Bort Lite

This pre-built apk gives a preview of the Bort SDK, without requiring a full
AOSP integration/build. Install on any device with `adb` access.

See the
[main Bort repo](https://github.com/memfault/bort/blob/master/CHANGELOG.md) for
changelog.

See [Documentation](https://mflt.io/bort-lite) for more details, including
limitations compared the full Bort SDK. A full feature matrix can be found
[here](https://mflt.io/android-features).

`adb` is required for installation: `brew install android-platform-tools`.

Download `bort-lite-release.zip` (contains apk and install script).

## Install Bort Lite

Mac/Linux

```
./install-bort-lite.sh <project-key> [root]
```

Windows

```
install-bort-lite.bat <project-key> [root]
```

A project key is required. Create a project in the Memfault dashboard before
installing Bort Lite.

Add `root` if running on a rooted device, to disable selinux enforcement on the
device (to enable more Bort features). This will output errors if device isn't
rooted (but Bort will still work). Only do this if you are happy to disable
selinux enforcement!

Dev Mode is enabled automatically. This will configure Bort to upload all data
immediately, and bypass device-side rate-limits. Consider also enabling
[Server-side Dev Mode](https://docs.memfault.com/docs/platform/rate-limiting/#server-side-developer-mode).

## Building

Unlike the full Bort SDK (which is built from source), Bort Lite is pre-built
and pre-signed for ease of use.
