# AOSP Project

### How to build ###

```bash
# Create dirs
$ mkdir aosp ; cd aosp

# Init repo
$ repo init --partial-clone -b android14-qpr2-release -u https://android.googlesource.com/platform/manifest

# Clone my local repo
$ git clone https://github.com/tnakamur/android_manifest_google_sunfish.git -b android-14 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh
$ lunch aosp_sunfish-userdebug
$ m
```

## Credits
2024 @tnakamur
