---
title: Receiver Not Detected
description: PC isn't recognizing your USB receiver dongle.
---

If no trackers appear in the SlimeVR Server window (not just one — all of them), the receiver is the likely culprit.

## 1. Confirm the receiver is plugged in

You should have:

- The **receiver dongle** plugged into the **USB extension cable**
- The **extension cable** plugged into your PC

:::caution[Always use the extension cable]
If you skipped the extension and plugged the receiver directly into your PC, **use the extension cable**. The receiver's USB connector is fragile and can be damaged by being plugged directly into a PC port repeatedly. The extension also dramatically improves wireless range.
:::

## 2. Does the OS see it?

**Windows:**

1. Open **Device Manager** (Win+X → Device Manager)
2. Expand **Human Interface Devices** or **Universal Serial Bus controllers**
3. Unplug the receiver, watch for which entry disappears
4. Plug back in — that entry should reappear

If nothing in Device Manager changes when you plug/unplug, the receiver isn't being seen at the OS level. Continue.

**macOS / Linux:**

In a terminal, run `lsusb` (Linux) or **System Information → USB** (macOS) and look for a Nordic Semiconductor USB device when the receiver is plugged in.

## 3. Try a different USB port

- Move to a known-good port (a port you know your keyboard or mouse works on)
- Avoid USB 3 ports that are also being used by your VR headset cable (USB 3 emits 2.4 GHz noise that interferes with the receiver)
- Avoid USB hubs for this test — go directly to the PC

## 4. Try a different cable

Bad USB cables are a leading cause of "device not detected." If you have a known-good USB-A extension cable lying around, try it. The included extension is usually fine, but it's worth ruling out.

## 5. Restart the SlimeVR Server

Sometimes the server fails to bind to the receiver on launch (especially if the receiver was plugged in mid-launch). Quit the server fully (system tray icon → Exit), wait a couple seconds, relaunch.

## 6. Restart the PC

If the OS gets confused about USB devices (common on Windows after sleep/wake cycles), a reboot clears it.

## 7. Reseat the receiver

Power off the PC, unplug everything from the receiver, plug back in, power on. Eliminates any USB hub state corruption.

## Still nothing

Reach out via [support](/support/) — receivers do occasionally fail. We'll work with you on a replacement.
