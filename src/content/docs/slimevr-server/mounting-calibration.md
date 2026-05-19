---
title: Mounting Calibration
description: Lock in tracker orientation so resets behave correctly.
---

Mounting calibration tells the server **which way each tracker is rotated on your body**. Without it, the server has no way to know whether the USB port is facing toward your foot, the floor, or your nose.

Run this once after assigning trackers to body parts, and again any time you remount a tracker in a different orientation.

## Through the setup wizard

The wizard prompts you through the calibration automatically. Strike the poses it asks for and click through.

## Manually

In the **Trackers** sidebar, choose **Mounting calibration**. The server will guide you through a standing pose, then a brief check pose. It only takes 10-15 seconds.

## Two ways to calibrate

There are two flavors of mounting calibration:

### Automatic (recommended)

Stand up straight, arms at your sides, facing forward. Click **Start**. The server reads the orientation of every tracker against your headset's facing direction and stores it. Done.

This is fast, accurate, and almost always what you want.

### Side calibration (per-tracker, from the tracker itself)

You can also trigger calibration on a single tracker by **double-pressing** its button. The tracker enters a brief calibration window — hold the body part in its neutral pose for a few seconds. Useful for fixing one tracker in the middle of a session without re-running the whole wizard.

## When to re-run mounting calibration

- You took a tracker off and put it back on a different way
- A strap rotated during a session
- One body part feels "off" while the rest feel right (often a sign that single tracker shifted)
- You replaced a tracker

## Things that aren't mounting calibration

- **IMU calibration** (factory-level sensor calibration) — already done at manufacture. Only matters if you replace your IMU, which you can't on IBIS trackers.
- **Full reset** — re-zeros rotation but uses the existing mounting offsets. You'll do this many times per session.

For the deep technical version of IMU calibration, see the upstream [SlimeVR IMU calibration page](https://docs.slimevr.dev/server/imu-calibration.html).
