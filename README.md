[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2020.png"/></center>](https://github.com/StatiXOS)

## Building Android ##
[Setting Up Build Environment](https://itz63c.github.io/posts/android-build-env/)

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b 11
```
## Sync Source ##
```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```
## Build Time (Linux x86_64 ONLY) ##
```bash
. build/envsetup.sh
brunch statix_<DEVICE>-userdebug (or statix_<DEVICE>-user)
```

XDA Thread Template: https://del.dog/statix-thread-template
