# AERA Recovery Project device tree for Realme GT8 Pro

Device codename: `lafa`

Platform: Qualcomm SM8850 (`canoe`)
Recovery partition limit: 100 MiB

This tree keeps the history of the original Realme conversion commits while
carrying the Realme GT8 Pro integration for AERA Recovery Project R1.0.

## Hardware support

- Display and touch
- File-based encryption
- A/B flashing, backup/restore, ADB, MTP, and fastbootd
- Wi-Fi
- Haptics and flashlight
- Adreno 840 recovery rendering with matching gen80200 firmware
- Qualcomm AGM/PAL audio using the installed Realme stock partitions
- KernelSU, KernelSU Next, and SukiSU Ultra support

The proprietary graphics and audio files in this repository target the
SM8850 OPlus platform used by `lafa`. They must be validated against the
matching Realme GT8 Pro stock firmware before release.

## Build

```sh
cd ~/Desktop/AERA_16.0
source build/envsetup.sh
lunch twrp_lafa-bp2a-eng
mka adbd recoveryimage
```

The output is written to `out/target/product/lafa/`.
