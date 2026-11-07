```
#include
/*
* Your warranty is now void.
*
* I am not responsible for bricked devices, dead SD cards,
* thermonuclear war, or you getting fired because the alarm app failed. Please
* do some research if you have any concerns about features included in this ROM
* before flashing it! YOU are choosing to make these modifications, and if
* you point the finger at me for messing up your device, I will laugh at you.
*/
```

# haretic: Android 17 with mainline-fork kernel for rabbit r1 (MT6765)
Flashable images for the rabbit r1, to be installed via [the haretic installer](https://github.com/haretic/installer)

Upstream Linux kernel 7.3 with driver forward ports from the MTK BSP kernel tree, running LineageOS 24 (Android 17).

LineageOS 24 was completely redesigned to fit a 480x640 screen.

Port status: beta, stable during runtime

## What works
removed - see https://github.com/haretic

# rabbitOS
rabbitOS imposed certain limitations on the hardware, obviously to save battery, which is a sensible thing to do on this device.
However, the haretic project endorses user choice, so these limitations have been removed.

- The CPU and GPU are allowed their full power budgets and overclock settings exist
- The charging circuitry limits can be configured.
- The screen refresh rate can be configured (the R1 panel is 100Hz capable)
- Thermal management is relaxed, to a safe point.
