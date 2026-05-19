---
title: Body Proportions
description: Tell SlimeVR how long your bones are so your avatar matches your real body.
---

A tracker only knows its rotation. To turn that into "your knee is here," the server needs to know the length of your femur, your tibia, your spine, etc. That's **body proportions**.

Wrong body proportions = avatar mismatch (legs too short, feet sinking into the floor, head poking through ceilings). Right body proportions = it just feels right.

## Two ways to set them

### AutoBone (recommended)

Recording-based calibration. You record short clips of yourself doing specific motions (standing, squatting, sometimes walking) while wearing the headset, and the server fits all bone lengths to your recordings simultaneously.

Steps:

1. In the SlimeVR window, open **Body proportions** → **AutoBone**.
2. Click **Start recording**. Put your headset on.
3. Follow the on-screen prompts (usually: stand, walk a bit, squat). Each segment is ~10 seconds.
4. Take the headset off, click **Apply**. The server updates all bone lengths.

AutoBone usually beats manual measurement, because it accounts for how *you specifically* wear your trackers — strap height, mounting offsets, etc.

### Manual

For each bone (hip width, torso, upper leg, lower leg, foot height, etc.) enter a measurement in centimeters. Measure with a tape from joint to joint.

This is faster than AutoBone if you've done it before and remember your numbers. New users should AutoBone first, then fine-tune individual bones manually.

## Fine-tuning

After AutoBone or manual entry, jump in VR and check:

- **Standing height** — your virtual eyes should be at your real-world eye height when you stand straight
- **Feet on the floor** — they should sit on the floor, not below or above it. Adjust **foot height** if not.
- **Hips** — should bend where your real hips do. If your avatar's legs feel detached from your torso, tweak **torso** length.

Small adjustments (a centimeter at a time) make a big visual difference. Iterate.

## When to re-measure

- After significant weight change
- After switching to different shoes (height differences matter)
- After remounting straps in a different position on your limbs

## More

The math behind AutoBone is documented upstream: [SlimeVR Body Proportions](https://docs.slimevr.dev/server/body-config.html).
