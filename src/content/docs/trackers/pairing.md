---
title: Pairing
description: Pair (or re-pair) an IBIS tracker to your USB receiver.
---

IBIS trackers ship **pre-paired to the receiver that came in your kit**. For most users, you don't need to do anything on this page — turn the trackers on, plug in the receiver, they connect.

You only need to pair manually if:

- You bought a single replacement/extra tracker
- You swapped to a new receiver
- A tracker has dropped off the receiver and isn't reconnecting after a power cycle
- You're recovering from a botched firmware update

## How pairing works

The receiver has its own radio ID. When a tracker is in pairing mode, it scans for any receiver advertising for pairing and binds to the first one it finds. Once paired, the tracker remembers that receiver and ignores all others.

:::caution[Receiver pairing today]
The current IBIS receiver does **not** have a hardware pairing button, and the SlimeVR Server does **not** yet expose receiver pairing in its UI. Until either is added, you put the receiver into pairing mode by sending the `pair` command over its USB serial port using **nRF Connect for Desktop's Serial Terminal** (Nordic Semiconductor's free toolset). The steps below walk through that workflow. This procedure follows the official [SlimeVR Smol Pairing & Calibration guide](https://docs.slimevr.dev/smol-slimes/firmware/smol-pairing-and-calibration.html).
:::

## Pair a single tracker

### 1. Open a serial terminal to the receiver

1. Install **[nRF Connect for Desktop](https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop)** if you don't already have it. From its app library, install the **Serial Terminal** app.
2. Plug the receiver into your PC via its **[USB extension cable](/receiver/installing/)** (do not plug it directly into the PC — the receiver's connector is fragile).
3. Open **Serial Terminal**. Select the receiver's serial port from the device dropdown. The terminal connects and you'll see receiver console output.

### 2. Put the receiver into pairing mode

In the Serial Terminal input, type:

```
pair
```

…and press Enter. The receiver is now listening for trackers.

### 3. Put the tracker into pairing mode

On the tracker, **press the button 3 times** in quick succession. The LED will start flashing **once per second**, indicating it's broadcasting for pairing.

### 4. Wait for the pair to register

Within a few seconds, the receiver's Serial Terminal will log a confirmation line like:

```
<inf> esb_event: Added device on id 0 with address 95CB23A0FDF7
```

The tracker's LED will stop the once-per-second pairing blink. The tracker now appears in the SlimeVR Server window.

### 5. Exit pairing mode

In the Serial Terminal, type:

```
exit
```

…and press Enter. The receiver returns to normal operation. If you forget this step, leaving the receiver in pairing mode is not harmful — it just keeps listening for new trackers.

### 6. Assign the tracker to a body part

See [Assigning Trackers](/slimevr-server/assigning-trackers/).

## Pair multiple trackers at once

After step 2, repeat step 3 for each tracker in turn while the receiver is still in pairing mode. The receiver logs an `esb_event: Added device on id N with address …` line for each new tracker. When you're done, run `exit` once.

## Other receiver serial commands

These commands work in the same Serial Terminal session. Source: [SlimeVR Smol Serial & Button Commands](https://docs.slimevr.dev/smol-slimes/firmware/smol-firmware-serial-and-button-commands.html).

| Command | What it does |
|---|---|
| `pair` | Enter pairing mode |
| `exit` | Exit pairing mode |
| `add <address>` | Manually add a tracker by its radio address |
| `remove` | Remove the last paired tracker |
| `clear` | Clear all stored trackers (you'll need to re-pair everything) |
| `reboot` | Soft-reset the receiver |
| `dfu` | Enter the DFU bootloader for firmware updates — see [Updating Firmware](/firmware/updating/) |

## Confirm a pair

Pick up the tracker and physically rotate it. The matching entry in the SlimeVR Server window should show its orientation changing in real time. If a different tracker animates, you've assigned the wrong physical tracker to that slot — re-assign in the [Assigning Trackers](/slimevr-server/assigning-trackers/) flow.

## When pairing fails

- **Tracker LED keeps blinking once per second:** The receiver isn't in pairing mode. Re-run `pair` in the Serial Terminal.
- **`pair` command does nothing in the terminal:** Confirm you're connected to the receiver's serial port (not another USB serial device) and that you actually pressed Enter after typing the command.
- **Tracker pairs but doesn't appear in SlimeVR:** Check the [SlimeVR Server window's connection status](/slimevr-server/first-launch/) and the [receiver troubleshooting page](/troubleshooting/receiver-not-detected/).
- **Tracker pairs to the wrong receiver** (e.g., a friend's): Hold the button to power off, then re-pair to your receiver using the steps above.
