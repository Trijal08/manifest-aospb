### Sync the source
```bash
        repo init -u https://github.com/aosp-pb/manifest -b 15
        repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j$(nproc --all)
```

### Build
```bash
        source build/envsetup.sh
        lunch aosp_$Device-ap3a-userdebug
        make bacon -j$(nproc --all) | tee log.log
```
