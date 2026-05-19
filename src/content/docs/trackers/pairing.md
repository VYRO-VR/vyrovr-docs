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

## Pair a single tracker

1. **Plug in the receiver** and launch the SlimeVR Server. Make sure the server window is visible.
2. **Put the receiver into pairing mode.** In the SlimeVR window, open the trackers list — there will be a pairing option for the receiver. Activate it. (If you have an older server build that doesn't expose this, see [Tracker Won't Pair](/troubleshooting/tracker-not-pairing/).)
3. **Put the tracker into pairing mode.** Press the button **3 times** in quick succession. The LED will start flashing rapidly.
4. **Wait for the pair.** Within a few seconds the rapid flash stops and the tracker either turns solid (if connected) or starts slowly blinking (if waiting to connect). The tracker now appears in the SlimeVR window.
5. **Assign it to a body part** — see [Assigning Trackers](/slimevr-server/assigning-trackers/).

## Pair multiple trackers at once

Repeat step 3 for each tracker in turn while the receiver is in pairing mode. The receiver can pair several trackers in a single session.

## Confirm a pair

Pick up the tracker and physically rotate it. The matching entry in the SlimeVR window should show its orientation changing in real time. If a different tracker animates, you've assigned the wrong physical tracker to that slot — re-assign in the [Assigning Trackers](/slimevr-server/assigning-trackers/) flow.

## When pairing fails

- **Tracker LED keeps blinking rapidly:** The receiver isn't in pairing mode. Re-trigger it.
- **Tracker pairs but doesn't appear:** Check the [SlimeVR Server window's connection status](/slimevr-server/first-launch/) and the [receiver troubleshooting page](/troubleshooting/receiver-not-detected/).
- **Tracker pairs to the wrong receiver** (e.g., a friend's): Hold the button to power off, then re-pair to your receiver.

