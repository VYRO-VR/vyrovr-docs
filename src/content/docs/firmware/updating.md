---
title: Updating Firmware
description: Update the firmware on your IBIS trackers and receiver using nRF Connect for Desktop.
---

IBIS firmware updates ship occasionally with bug fixes and new features. Updates are **optional** — your hardware works fine on whatever firmware it shipped with. Update when you want a specific new feature or when the [VYRO VR Discord](https://discord.gg/vyrovr) flags an important fix.

:::caution
**Do not** use the **Update firmware** button inside the SlimeVR Server window. That flow is for ESP/Wi-Fi-based SlimeVR trackers and does **not** apply to IBIS trackers or their receiver, which are nRF-based. Use the nRF Connect for Desktop workflow on this page instead.
:::

## When to update

- VYRO VR posts a known-good firmware release with fixes
- You're troubleshooting an issue that's known to be fixed in newer firmware
- A new SlimeVR Server feature requires updated firmware (rare; the server announces this)

If everything is working, **don't update for the sake of it**. Stable firmware in production is good firmware.

## Tool: nRF Connect for Desktop

Both trackers and the receiver are flashed with **[nRF Connect for Desktop](https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop)** — Nordic Semiconductor's free toolset. You'll use two apps from inside it:

- **Programmer** — flashes new firmware over USB
- **Serial Terminal** — talks to the receiver over its serial port to confirm version and status after a flash

Install nRF Connect for Desktop for your OS, launch it, and install the **Programmer** and **Serial Terminal** apps from the in-app library.

## Updating a tracker

1. Download the latest tracker firmware image VYRO VR points you at (usually a `.hex` or `.zip` file).
2. Put the tracker into **DFU mode** — press the button **4–5 times** in quick succession. The LED switches to a slow flutter pattern. See [DFU Mode](/firmware/dfu-mode/).
3. Plug the tracker into your PC over USB-C.
4. Open **Programmer**, select the tracker from the device dropdown, drag in the firmware file, and click **Write**.
5. Wait for the flash to finish. Do not unplug or power-cycle the tracker mid-flash.
6. Once the Programmer reports success, power-cycle the tracker (hold to off, single-press to on). It should reconnect to the receiver — pairing is preserved across firmware updates.

If the tracker doesn't reconnect after a power-cycle, re-pair it: [Pairing](/trackers/pairing/).

## Updating the receiver

1. Download the latest receiver firmware image VYRO VR points you at.
2. Plug the receiver into your PC over USB.
3. Open **Programmer**, select the receiver from the device dropdown, drag in the firmware file, and click **Write**. Wait for the flash to finish.
4. Open **Serial Terminal**, connect to the receiver's serial port, and confirm the firmware version reported matches what you flashed.
5. Re-launch the SlimeVR Server and confirm trackers reconnect.

## If an update fails mid-flash

A **tracker** that interrupts mid-flash stays in **DFU mode** (slow LED flutter) — re-run the tracker steps above with the previous known-good firmware. See [DFU Mode](/firmware/dfu-mode/) for recovery details.

A **receiver** that interrupts mid-flash usually stays visible to nRF Connect for Desktop's **Programmer** — re-flash with the previous known-good image from the same workflow above.
