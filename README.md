# Project Infinity-X for OnePlus 12 (waffle)

Unofficial Android 17 build setup for the OnePlus 12.

- Device: OnePlus 12
- Codename: waffle
- ROM: Project Infinity-X
- Android: 17
- Variant: userdebug
- Build type: unofficial
- GApps: included

## Source

https://github.com/ProjectInfinity-X/manifest

Branch: `17`

## Device tree forks

- https://github.com/Dipraj63/android_device_oneplus_waffle
- https://github.com/Dipraj63/android_device_oneplus_sm8650-common

## Included repositories

The `waffle.xml` manifest includes the device trees, kernel, kernel modules, kernel device trees, Pixelworks interfaces, Oplus hardware, and OnePlus proprietary vendor repositories.

## Build instructions

### 1. Initialize source

    mkdir -p ~/InfinityX
    cd ~/InfinityX
    repo init -u https://github.com/ProjectInfinity-X/manifest.git -b 17

### 2. Add this local manifest

    git clone https://github.com/Dipraj63/Project-Infinity-X-Waffle.git /tmp/waffle-setup
    mkdir -p .repo/local_manifests
    cp /tmp/waffle-setup/waffle.xml .repo/local_manifests/

### 3. Sync

    repo sync -c -j4

### 4. Configure

    source build/envsetup.sh
    lunch infinity_waffle-userdebug

### 5. Build

    m bacon -j4

Output: `out/target/product/waffle/`

## Build notes

- Dolby integration is temporarily disabled because its configuration was unavailable.
- Proprietary vendor components remain subject to their respective licenses.
- Successful compilation does not guarantee that every feature works or that the ROM has been boot-tested.

## Build verification

On November 25, 2026, an Android 17 GApps userdebug build completed successfully. The generated ZIP passed `unzip -t` integrity verification.

## Credits

- Project Infinity-X
- LineageOS
- crDroid
- TheMuppets
- OnePlus device development community
### 4. Configure

    source build/envsetup.sh
    lunch infinity_waffle-userdebug

### 5. Build

    m bacon -j4

Output: `out/target/product/waffle/`

## Build notes

- Dolby integration is temporarily disabled because its configuration was unavailable.
- Proprietary vendor components remain subject to their respective licenses.
- Successful compilation does not guarantee that every feature works or that the ROM has been boot-tested.

## Build verification

On November 25, 2026, an Android 17 GApps userdebug build completed successfully. The generated ZIP passed `unzip -t` integrity verification.

## Credits

- Project Infinity-X
- LineageOS
- crDroid
- TheMuppets
- OnePlus device development community
