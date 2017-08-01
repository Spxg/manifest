# HOW-TO Build

* Initialize the repository
   ```sh
   repo init -u ssh://git@github.com/LineageOS/android.git -b cm-14.1
 　```
* Add my manifest to the .repo folder (don't worry about the alert you will get about being DEPRECATED)
   ```sh
   cp local_manifest.xml .repo/
   ```
* Sync latest LineageOS 14.1 sources
   ```sh
   repo sync -j20 --force-sync
 　```
* Apply all Patches
   ```sh
   ./Exynos5410_patcher/patch.sh
   ```
* You are good to go, proceed with the compiling process
OPTIONAL (if you want built-in root support):
   ```sh
   export WITH_SU=true
　 ```
* FOR SCH-I959 (ja3gduosctc) only. OTHERWISE, REPLACE THE CODENAME WITH OTHERS SUPPORTED (check the manifest).
   ```sh
   .build/envsetup.sh && lunch lineage_ja3gduosctc-userdebug
   ```
   ```sh
   brunch lineage_ja3gduosctc-userdebug
   ```
