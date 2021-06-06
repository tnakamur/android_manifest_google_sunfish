# TKernel

### How to build ###

```bash
# Create dirs
$ mkdir aosp ; cd aosp

# Init repo
$ repo init --depth=1 -u https://android.googlesource.com/platform/manifest -b android-11.0.0_r36

# Clone my local repo
$ git clone https://github.com/tnakamur/android_manifest_google_sunfish.git -b tkernel-11 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh
$ lunch aosp_sunfish-eng
$ make bootimage
```

## Credits
2021 @tnakamur
