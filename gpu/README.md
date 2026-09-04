# Realme GT8 Pro GPU recovery prebuilts

This directory carries the SM8850 Adreno 840 recovery userspace, KGSL module,
and gen80200 firmware inherited by the initial `lafa` bring-up. These files are
kept device-local because their ABI must match the device kernel and firmware.

Before release, validate every proprietary component against the matching
Realme GT8 Pro stock OTA and replace any inherited component whose hash or ABI
does not match the production firmware.

`msm_kgsl.ko` is loaded by AERA's dependency-aware vendor-module loader. The
native-window ABI is packaged unmodified so the Adreno driver and mapper stack
see the interface expected by this SM8850 platform.
