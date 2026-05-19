---
title: Stay Aligned
description: Auto-correct yaw drift while you play.
---

**Stay Aligned** is a SlimeVR Server feature (0.16.0+) that automatically corrects **yaw drift** while you play. Instead of yaw-resetting every few minutes, the server detects when a tracker's facing direction has drifted and quietly nudges it back.

## What yaw drift is

Yaw drift is the slow rotation of your virtual heading away from your real heading over time. It comes from tiny IMU integration errors that accumulate while you move. Without correction, after 20-30 minutes your avatar might be facing 10° off from where you're actually facing.

Yaw drift is the most annoying form of drift because it makes your virtual feet face the wrong way. Stay Aligned eliminates most of it.

## Enabling it

1. Open the SlimeVR Server
2. **Settings → Trackers / Drift** (the exact label depends on server version)
3. Toggle **Stay Aligned** on

That's it. There's no per-tracker config; the server applies it across all paired trackers.

## What changes

- You'll yaw-reset less often. Most users go from every 10 minutes to once per session or less.
- Trackers feel "stickier" in the right direction.
- No latency cost — the corrections happen at idle moments.

## What doesn't change

- **Pitch and roll** drift still exist, though they're less severe. Full reset still occasionally needed.
- **Position errors** from wrong body proportions aren't affected — Stay Aligned is purely a rotation feature.
- Mounting and pairing work the same.

## Requirements

- SlimeVR Server **0.16.0 or newer**
- Firmware that supports it (recent IBIS firmware does; check Discord for older units)

## See also

Original SlimeVR write-up from the maintainers: [SlimeVR 0.16 Stay Aligned release notes](https://vyrovr.com/blogs/news/slimevr-server-update-introduces-stay-aligned) (mirrored on VYRO's blog).
