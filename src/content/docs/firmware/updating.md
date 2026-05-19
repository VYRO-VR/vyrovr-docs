---
title: Updating Firmware
description: Update the firmware on your IBIS trackers.
---

IBIS firmware updates ship occasionally with bug fixes and new features. Updates are **optional** — your trackers work fine on whatever firmware they shipped with. Update when you want a specific new feature or when [VYRO Discord](https://discord.gg/vyrovr) flags an important fix.

## When to update

- A new SlimeVR Server feature requires updated firmware (rare; the server announces this)
- VYRO posts a known-good firmware release with fixes
- You're troubleshooting an issue that's known to be fixed in newer firmware

If everything is working, **don't update for the sake of it**. Stable firmware in production is good firmware.

## How to update

Updates are done with the **SmolSlimeConfigurator** tool (or the SlimeVR Server's built-in firmware update flow when available).

### Using SlimeVR Server (when supported)

1. Plug the receiver in, power on the tracker
2. In the SlimeVR window, open the tracker's detail panel
3. If a firmware update is available, you'll see an **Update firmware** button
4. Click, wait, done

### Using SmolSlimeConfigurator

If the server-based path isn't available:

1. Download the latest SmolSlimeConfigurator from the [SlimeVR project](https://docs.slimevr.dev/smol-slimes/firmware/SmolSlimeConfigurator.html)
2. Connect the tracker over USB (USB-C cable directly into the tracker)
3. Open the tool, select the tracker, choose the firmware version
4. Click **Flash**. Don't unplug until it's done.

## After updating

- **Power-cycle** the tracker (hold to off, single-press to on)
- It should reconnect to the receiver immediately (the pairing is preserved across firmware updates in normal flows)
- If it doesn't reconnect, re-pair it: [Pairing](/trackers/pairing/)

## If an update fails mid-flash

The tracker boots into **DFU mode** automatically (slow LED flutter) — you can retry the flash. See [DFU Mode](/firmware/dfu-mode/).

## Deep technical reference

Full SmolSlimeConfigurator docs (multi-tracker batches, advanced options): [SlimeVR upstream docs](https://docs.slimevr.dev/smol-slimes/firmware/SmolSlimeConfigurator.html).
