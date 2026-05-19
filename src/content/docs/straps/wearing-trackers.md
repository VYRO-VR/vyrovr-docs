---
title: Wearing Trackers
description: Where each IBIS tracker goes on your body, and which way is "up."
---

This is the reference page for **placement**. Get this right and your tracking will be solid. Get this wrong and every reset will fight you.

The good news: SlimeVR's mounting calibration is forgiving about exact rotation. As long as the tracker is on the right body part and roughly flat against the limb, the wizard figures out the rest.

## General rules

1. **Mount trackers where muscle movement won't shift them.** You want the tracker to follow your bones, not your soft tissue. Pick the spot on each limb where flexing the muscle nearby moves the tracker as little as possible.
2. **Snug, not tight.** A tracker that slides during use will confuse the server every time you move.
3. **USB port faces down** (for limb-mounted trackers). This keeps the tracker oriented consistently and makes the button easy to find.
4. **Don't worry about perfect rotation.** Mounting calibration handles offsets.

## Lower body (Core kit and up)

### Thigh

- **Position:** mid-thigh, on the side or front of the leg, where flexing the quad shifts the tracker as little as possible
- **Orientation:** USB port toward the foot
- **Tightness:** firm enough that flexing the quad doesn't shift it

### Lower leg / shin

- **Position:** on the calf, just below the widest part, on a spot that doesn't shift when you flex
- **Orientation:** USB port toward the foot
- **Tightness:** snug; calves shift less than thighs so this is forgiving

### Hip / waist

- **Position:** on the **lower back**, just above the tailbone, centered
- **Orientation:** USB port down
- **Tightness:** the strap goes around the waist; tighten until it doesn't ride up or down when you twist

The lower-back position is correct — **not** the front of the hip. Your spine pivots from the lower back, so that's where the tracker needs to be for the avatar's hip to track yours.

## Upper body

### Upper arm

- **Position:** as close to the elbow as possible, on the upper arm (above the elbow joint, not on it)
- **Orientation:** flat face up toward the ceiling when you T-pose (arms held straight out to the sides)
- **Tightness:** snug; arms move a lot, so err on the firmer side

Per [SlimeVR's guidance](https://docs.slimevr.dev/server/putting-on-trackers.html), the upper-arm tracker goes "above the elbow, on the side or back" with the "front" face toward the ceiling when T-posed.

### Chest

- **Position:** anywhere on or above the chest, via the included [chest harness](/straps/chest-harness/). **Higher is better** — mount toward the upper chest rather than low on the ribs.
- **Orientation:** USB port down

## Feet

If you have the [Foot Tracker Upgrade Kit](/straps/foot-kit/):

- **Position:** top of the foot (instep) — **only**. Do not mount foot trackers on the shin or ankle.
- **Orientation:** "up" face toward the ankle, "front" face toward the ceiling — per [SlimeVR's mounting guidance](https://docs.slimevr.dev/server/putting-on-trackers.html)
- **Tightness:** snug but not painful; remember you'll be walking

## Final sanity check

Once everything's strapped on, look at the SlimeVR Server window. Each tracker should be live (orientation arrow moving in real time when you rotate the body part). If something doesn't move when you expect, you've put the wrong tracker on that body part — re-assign in the [Assigning Trackers](/slimevr-server/assigning-trackers/) step.

Then run **mounting calibration** ([details](/slimevr-server/mounting-calibration/)) to lock in orientation. You're good.
