---
title: LED Codes
description: What each LED pattern on an IBIS tracker means.
---

The IBIS tracker has a single LED that uses different on/off patterns to communicate state. Use this page as a reference when something looks off.

## Connection states

| Pattern | Meaning |
|---|---|
| Solid on | Powered and connected to the receiver |
| Slow blink (once per second) | Powered, searching for receiver |
| Rapid blink (several times per second) | **Pairing mode** — see [Pairing](/trackers/pairing/) |
| LED off after a press | Powered off |

## Charging states

When the tracker is sitting in the charging dock:

| Pattern | Meaning |
|---|---|
| Solid charging LED | Currently charging |
| Charging LED off (with USB plugged in) | Fully charged, or no charge current |

## Battery warnings

| Pattern | Meaning |
|---|---|
| Periodic double-blink while in use | Low battery — top up soon |
| Tracker drops off and won't power back on | Battery empty; recharge before retrying |

## Firmware / DFU

| Pattern | Meaning |
|---|---|
| Distinct slow flutter on boot | DFU (firmware update) mode — entered via 4–5 button presses |

If you didn't mean to enter DFU mode, just power-cycle (hold the button to power off, then single-press to start).

:::note
Some patterns are firmware-version dependent. If your tracker's LED is doing something you can't find here, post a short clip in the [VYRO VR Discord](https://discord.gg/vyrovr) — easiest way to identify it and improve this page.
:::

## See also

- [Pairing](/trackers/pairing/)
- [Powering On & Off](/trackers/powering-on-off/)
- [Charging](/charging-and-battery/charging/)
