[<center><img src="https://i.imgur.com/osNyVek.png" height="50%" width="50%;"/></center>](https://github.com/StatiXOS)

## Building Android ##
[Setting Up Build Environment](https://raw.githubusercontent.com/nathanchance/Android-Tools/master/Guides/Building_AOSP.txt)

## REMINDER ##
Be sure to check the manifest branch depending on your device.

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b 10
```

### OR ###
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b 10-caf
```
depending on your device.

## Sync Source ##
```bash
repo sync -c -f  --no-tag --no-clone-bundle -j$(nproc --all)
```
## Build Time (Linux x86_64 ONLY) ##
```bash
. build/envsetup.sh
brunch statix_<DEVICE>-userdebug (or statix_<DEVICE>-user)
```
