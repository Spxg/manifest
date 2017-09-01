# HOW-TO Build
* Initialize the repository
   
   ```sh
   repo init -u git://github.com/LineageOS/android.git -b cm-14.1
* Add my manifest to the .repo folder (don't worry about the alert you will get about being DEPRECATED)
   
   
   ```sh
   cp local_manifest.xml .repo/
* Sync latest LineageOS 14.1 sources
  
  
  ```sh
   repo sync -j20 --force-sync
* Apply all Patches
   
   
   ```sh
   ./Exynos5410_patcher/patch.sh
* You are good to go, proceed with the compiling process
OPTIONAL (if you want built-in root support):
   
   
   ```sh
   export WITH_SU=true

