# haretic: Android 17 with mainline-fork kernel for rabbit R1 (MT6765)
Flashable images for the rabbit R1, to be installed the same way the original rabbit firmware package is, or via mtkclient.
Upstream Linux kernel 7.1 with driver forward ports from the MTK BSP kernel tree, running LineageOS 24 (Android 17).

Port status: alpha

stable during runtime, not quite ready as daily driver yet. power consumption remains the biggest hurdle.

## What works
- WiFi
- Bluetooth
- BLE
- RIL/Mobile data (telephony untested)
- SoC sleep states: CPU idle through MCDI, including cluster power-off
- Display with PowerVR GE8320 GPU acceleration (stock RabbitOS userspace on a ported DDK 1.13 kernel driver)
- Touchscreen, side button and scroll wheel
- Camera (Hi-846) through libcamera with a software ISP, front and back by turning the motor
- Accelerometer and gyroscope
- Audio: speaker and microphone
- GPS
- Hardware video encode/decode (Codec2)
- Battery, fuel gauge and charging, with Lineage charging limit (down to 50%)
- USB device mode and adb
- Encrypted /data (FBE), release-keys signed builds, A/B updates

## What doesn't
- SoC deep sleep (SPM suspend): the device suspends to idle only (WIP)
- Calls and SMS untested
- Camera runs at reduced resolution/frame rate (CPU debayering, no hardware ISP)

# rabbitOS
rabbitOS imposed certain limitations on the hardware, obviously to save battery, which is a sensible thing to do on this device.
However, the haretic project endorses user choice, so these limitations have been removed.

- The CPU and GPU are allowed their full power budgets.
- The charging circuitry limits can be configured.
- The screen refresh rate can be configured (the R1 panel is 100Hz capable)
- Thermal management is relaxed, to a safe point.
