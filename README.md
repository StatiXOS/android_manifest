[<center><img src="https://i.imgur.com/osNyVek.png" height="50%" width="50%;"/></center>](https://github.com/StatiXOS)

## Building Android ##
[Setting Up Build Environment](https://raw.githubusercontent.com/nathanchance/Android-Tools/master/Guides/Building_AOSP.txt)

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b 9
```
## Sync Source ##
```bash
repo sync -c -f --force-sync --no-tag --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```
## Build Time (Linux x86_64 ONLY) ##
```bash
. build/envsetup.sh
lunch statix_<DEVICE>-userdebug (or statix_<DEVICE>-user)
time m -j$(nproc --all) bacon
```
