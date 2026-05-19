---
title: IBIS Tracker Overview
description: Specs, controls, and at-a-glance reference for IBIS trackers.
---

The IBIS tracker is VYRO-VR's SlimeVR-compatible full-body tracker. This page is a quick reference; deeper instructions live under the section pages.

## Specs

| | |
|---|---|
| Weight | ~11 g |
| Height | < 8 mm |
| Battery life | 50+ hours per charge |
| IMU | LSM6DSV |
| Microcontroller | Nordic nRF52 family |
| Wireless | 2.4 GHz proprietary (via included USB receiver) |
| Charging | USB-C, via included charging dock |
| Auto-sleep | After 15 minutes idle |

## Controls

There is **one button** on the tracker. Different press counts do different things.

| Action | Result |
|---|---|
| 1 press | Power on / **reset** (when already on) |
| 2 presses | Enter **side-calibration** mode |
| 3 presses | Enter **pairing** mode |
| 4–5 presses | Enter **DFU** (firmware-update) mode — avoid unless intentional |
| Hold | Power off |

:::caution
The button behavior above is current as of the last shipping firmware we documented. If you're on very recent firmware and it doesn't match, check the [Discord](https://discord.gg/vyrovr) — and let us know so we can update this page.
:::

## LED at a glance

| LED behavior | Meaning |
|---|---|
| Solid on | Powered, connected to receiver |
| Slow blink | Powered, not yet connected |
| Rapid blink | Pairing mode (3 presses) |
| Pulse pattern | See [LED Codes](/trackers/led-codes/) for full reference |

## Where to go next

- First-time setup → [Quick Start](/getting-started/quick-start/)
- Pair / re-pair a tracker → [Pairing](/trackers/pairing/)
- Power and sleep behavior → [Powering On & Off](/trackers/powering-on-off/)
- Full LED reference → [LED Codes](/trackers/led-codes/)
