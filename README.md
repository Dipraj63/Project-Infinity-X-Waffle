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

## Exact source revisions

The following commits were used in the successful November 25, 2026 build.

| Component | Repository | Commit |
|---|---|---|
| OnePlus 12 device tree | Dipraj63/android_device_oneplus_waffle | `9d95f5b62b33509fe30d01524fa658ac7403eb46` |
| SM8650 common device tree | Dipraj63/android_device_oneplus_sm8650-common | `0ed212c0060999e705e693e6fe74c55b5226c3e8` |
| SM8650 kernel | crdroidandroid/android_kernel_oneplus_sm8650 | `4091cd2fbe730d381ea79bfa5506c83fbaf464c5` |
| Kernel modules | crdroidandroid/android_kernel_oneplus_sm8650-modules | `1ae1387774a8915beff1669a65104f13e8299440` |
| Kernel device trees | LineageOS/android_kernel_oneplus_sm8650-devicetrees | `efac9372a17132e9c6ff437cf8869c9e6de546e1` |
| Pixelworks interfaces | LineageOS/android_hardware_pixelworks_interfaces | `80fa86ece0ab820b02ff059bc1c1b1f9e5f219a3` |
| Oplus hardware | crdroidandroid/android_hardware_oplus | `8778fab10bf33043804edd9c434f7ab3851a9c71` |
| OnePlus 12 vendor | TheMuppets/proprietary_vendor_oneplus_waffle | `4705e2085992a19b2a3724d536841f604220fcaa` |
| SM8650 common vendor | TheMuppets/proprietary_vendor_oneplus_sm8650-common | `0f5e25894a2573daf6216a13ebd7116866015862` |
| OnePlus IR vendor | crdroidandroid/proprietary_vendor_oneplus_ir | `c398de3b34c2c6ae03a75da8dad3971f75b275d2` |

A complete resolved manifest is included as `waffle-pinned.xml`. It records the exact revisions of all synced projects.
