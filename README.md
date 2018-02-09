# static_manifest

Repo init command:

	repo init -u https://github.com/StatiXOS/android_manifest.git -b 8.1-linux

Sync Source

	repo sync -c -f --force-sync --no-tag --no-clone-bundle -j$(nproc --all)

To build (Linux x86_64 ONLY):

        . build/envsetup.sh
        lunch aosp_angler-userdebug
        time m -j6 bacon
