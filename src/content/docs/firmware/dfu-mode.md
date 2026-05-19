---
title: DFU Mode
description: What DFU mode is, how to enter (and exit) it, and when you'd want to.
---

**DFU** stands for **Device Firmware Update**. It's a special boot mode where the tracker only runs its bootloader, not normal firmware. While in DFU you can flash a new firmware image — including recovery from a botched flash.

You should not enter DFU mode by accident. If you did, follow the **exit** section below.

## When you actually want DFU mode

- A firmware update failed mid-way and the tracker won't boot normally
- You're manually flashing a development firmware build
- The configurator tool tells you to put a tracker in DFU mode

## How to enter DFU mode

**Press the button 4 or 5 times** in quick succession. The tracker enters DFU mode and the LED switches to a distinctive slow flutter pattern.

In this mode the tracker advertises a USB-mass-storage bootloader endpoint. Plug it in over USB-C and your OS will see a small drive (or expose it to the configurator tool).

## How to exit DFU mode (you didn't mean to enter it)

**Power-cycle** the tracker:

1. **Hold the button** until any LED activity stops
2. **Single-press** to power on normally

The tracker boots into normal firmware. Crisis averted.

## DFU mode does not erase your tracker

Entering DFU mode is non-destructive. Pairing, calibration, and stored config all survive. The only way to lose those is to actually flash a different firmware image — and even then, re-pairing is fast.

## Recovering from a failed flash

If a firmware update failed and the tracker is stuck:

1. Confirm it's in DFU mode (slow flutter LED, USB drive shows up when plugged into PC)
2. Run SmolSlimeConfigurator or the SlimeVR Server firmware tool with the **previous known-good firmware**
3. Flash, wait for completion, power-cycle
4. Re-pair if needed: [Pairing](/trackers/pairing/)

If the tracker isn't appearing as a USB device at all (no flutter, no drive), check the cable first — many "dead" trackers are dead USB-C cables.

## Deeper reference

The bootloader internals are covered upstream: [SlimeVR Smol flashing](https://docs.slimevr.dev/smol-slimes/firmware/smol-flashing-firmware.html).
