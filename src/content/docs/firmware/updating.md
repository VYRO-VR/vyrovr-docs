---
title: Updating Firmware
description: Update the firmware on your IBIS trackers and receiver.
---

IBIS firmware updates ship occasionally with bug fixes and new features. Updates are **optional** — your hardware works fine on whatever firmware it shipped with. Update when you want a specific new feature or when the [VYRO VR Discord](https://discord.gg/vyrovr) flags an important fix.

## When to update

- A new SlimeVR Server feature requires updated firmware (rare; the server announces this)
- VYRO VR posts a known-good firmware release with fixes
- You're troubleshooting an issue that's known to be fixed in newer firmware

If everything is working, **don't update for the sake of it**. Stable firmware in production is good firmware.

## Updating trackers

Tracker firmware is updated through the **SlimeVR Server**:

1. Plug the receiver in, power on the tracker.
2. In the SlimeVR Server window, open the tracker's detail panel.
3. If a firmware update is available, you'll see an **Update firmware** button.
4. Click it and wait until the server reports the flash is complete. Do not unplug or power-cycle the tracker mid-flash.
5. Power-cycle the tracker (hold to off, single-press to on). It should reconnect to the receiver immediately — pairing is preserved across firmware updates.

If the tracker doesn't reconnect after a power-cycle, re-pair it: [Pairing](/trackers/pairing/).

## Updating the receiver

Receiver firmware is updated with **[nRF Connect for Desktop](https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop)** — Nordic Semiconductor's free toolset.

You need two apps from inside nRF Connect for Desktop:

- **Programmer** — flashes new firmware onto the receiver
- **Serial Terminal** — talks to the receiver over USB to confirm version, status, and post-flash behavior

### Steps

1. Install **nRF Connect for Desktop** for your OS, launch it, and install the **Programmer** and **Serial Terminal** apps from the app library.
2. Download the latest receiver firmware image from the release notes VYRO VR points you at (usually a `.hex` or `.zip` file).
3. Plug the receiver into your PC over USB.
4. Open **Programmer**, select the receiver from the device dropdown, drag in the firmware file, and click **Write**. Wait for the flash to finish.
5. Open **Serial Terminal**, connect to the receiver's serial port, and confirm the firmware version reported matches what you flashed.
6. Re-launch the SlimeVR Server and confirm trackers reconnect.

## If an update fails mid-flash

A tracker that interrupts mid-flash boots into **DFU mode** automatically (slow LED flutter) — see [DFU Mode](/firmware/dfu-mode/) for recovery.

A receiver that fails mid-flash usually stays visible to nRF Connect for Desktop's **Programmer** — re-flash with the previous known-good image from the same workflow above.
