[<center><img src="https://i.imgur.com/osNyVek.png" height="50%" width="50%;"/></center>](https://github.com/StatiXOS)

## Building Android ##
[Setting Up Build Environment](https://raw.githubusercontent.com/nathanchance/Android-Tools/master/Guides/Building_AOSP.txt)

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b 10
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
