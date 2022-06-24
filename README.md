[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2020.png"/></center>](https://github.com/StatiXOS)

## Building Android ##
Your one-stop destination for all the documentation about building Android can be found [here](https://source.android.com/setup/build/building).

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


XDA Thread Template: https://del.dog/statix-thread-template
