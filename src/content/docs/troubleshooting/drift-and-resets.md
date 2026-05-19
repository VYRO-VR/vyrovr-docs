---
title: Drift & Resets
description: Avatar facing the wrong way, feet wandering, body misaligned — fix drift.
---

Drift is normal in any inertial tracking system, including SlimeVR. The question is "how often is it bad enough to be noticeable?" — and the answer should be "rarely, with a yaw reset now and then."

If you find yourself resetting constantly, something deeper is off.

## Quick checklist

1. **Did you full-reset at session start?** Stand straight, face forward, trigger full reset. Don't skip this.
2. **Is Stay Aligned on?** See [Stay Aligned](/firmware/stay-aligned/). It eliminates most yaw drift automatically.
3. **Are your body proportions correct?** Wrong torso length looks like drift even though it isn't. Re-run [AutoBone](/slimevr-server/body-proportions/).
4. **Did you run mounting calibration?** Without it, the server is guessing at orientation. Re-run [Mounting Calibration](/slimevr-server/mounting-calibration/).

## Common symptoms

### "My avatar is facing 10° off"

Trigger a **yaw reset**. If you have to do this every few minutes, enable [Stay Aligned](/firmware/stay-aligned/).

### "My feet are facing the wrong way" or "Knees bend backward"

Mounting on those trackers is wrong. Re-run [Mounting Calibration](/slimevr-server/mounting-calibration/) with the trackers worn correctly (USB ports down, on the calf/thigh muscle belly, not on a joint).

### "My avatar is leaning forward / hunched"

Hip tracker is mounted too high (in the small of your back rather than on the lower back) or rotated wrong. Re-check placement on [Wearing Trackers](/straps/wearing-trackers/).

### "One leg is drifting much faster than the other"

A single tracker may have a hardware quirk. Try swapping its body-part assignment with a different tracker (e.g., move the left-thigh tracker to right-thigh). If the drift follows the tracker, that tracker is the problem — reach out via [support](/support/).

### "Drift gets bad when I do fast turns"

This is normal in inertial tracking. Fast yaw motion accumulates errors. Mitigations: Stay Aligned, more frequent yaw resets, and a stationary moment between turns.

## When resets aren't fixing anything

If you reset, it looks right for a second, then immediately drifts again:

- Trackers shifted on the strap (re-tighten, re-do mounting calibration)
- Wrong body location assignment (swap two trackers — see [Assigning Trackers](/slimevr-server/assigning-trackers/))
- Receiver placement is so bad that a tracker is intermittently disconnecting — see [Range & Placement](/receiver/range-and-placement/)
