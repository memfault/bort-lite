# Bort Lite

This pre-built apk gives a preview of the Bort SDK, without requiring a full
AOSP integration/build. Install on any device with `adb` access.

See the main Bort repo for changelog.

See [Documentation](https://todo) for more details, including limitations
compared the full Bort SDK.

`adb` is required for installation: `brew install android-platform-tools`.

Download `bort-lite-release.zip` (contains apk and install script).

Install Bort Lite:

```
./install-bort-lite.sh <project-key> [root]
```

A project key is required. Create a project in the Memfault dashboard before
installing Bort Lite.

Add `root` if running on a rooted device, to disable selinux enforcement on the
device (to enable more Bort features). This will output errors if device isn't
rooted (but Bort will still work). Only do this if you are happy to disable
selinux enforcement!

Once installed, you can use Dev Mode to trigger actions (`bort_cli.py` is
available in the main Bort repo):

```
bort_cli.py dev-mode --bort-app-id com.memfault.bort.lite --enabled true
```

(Enabling dev mode will configure Bort to upload all data immediately, and
bypass device-side rate-limits).

Collect metrics (once Dev Mode is enabled):

```
bort_cli.py request-metrics --bort-app-id com.memfault.bort.lite
```

## Building

Unlike the full Bort SDK (which is built from source), Bort Lite is pre-built
and pre-signed for ease of use.

If you wish to build the Bort Lite apk locally, please contact Memfault support.
