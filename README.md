### Spinning up the environment
--------------
```bash
        bash <(curl -sL https://raw.githubusercontent.com/akhilnarang/scripts/refs/heads/master/setup/android_build_env.sh)
```

### Sync the source
--------------
```bash
mkdir aospb && cd aospb
repo init -u https://github.com/Trijal08/manifest-aospb -b 15
repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j$(nproc --all)
```

### Build
--------------
```bash
        source build/envsetup.sh
        lunch aosp_$Device-ap3a-userdebug
        make bacon -j$(nproc --all) | tee log.log
```

### Credits
--------------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**AOSPA**](https://github.com/AOSPA)
 * [**HentaiOS**](https://github.com/hentaios)
 * [**Project Radiant**](https://github.com/ProjectRadiant)
 * [**PixelOS-AOSP**](https://github.com/PixelOS-AOSP)
 * [**StatixOS**](https://github.com/StatiXOS)
 * [**Project Pixelage**](https://github.com/ProjectPixelage)
 * [**cAOSP**](https://github.com/c0smic-Lab)
 * ... And the list never ends.
