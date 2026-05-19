---
title: How the Trackers Work
description: A plain-English overview of what an IBIS tracker is doing under the hood.
---

You don't need to understand any of this to use the trackers. But if you're the kind of person who likes to know what's going on, this page is for you.

## The short version

Each IBIS tracker is a tiny circuit board with a **motion sensor (IMU)** and a **radio**. The IMU measures how the tracker is rotating in space, many times per second. The radio sends that data over **2.4 GHz wireless** to a **USB receiver dongle** plugged into your PC.

The **SlimeVR Server** running on your PC takes orientation data from every tracker, combines it with your body proportions, figures out where each of your limbs is, and feeds that into SteamVR (or VRChat OSC) as virtual full-body trackers.

That's the whole stack:

```
[IBIS tracker IMU] → [2.4GHz radio] → [USB receiver] → [SlimeVR Server] → [SteamVR / OSC] → [game]
```

## Why "nRF"?

IBIS trackers use a Nordic **nRF52** microcontroller with a built-in 2.4 GHz radio (the same family of chip you'll find in many Bluetooth devices, but here we use a custom low-latency protocol). That's the "nRF" in nRF-based SlimeVR designs.

The advantage over Wi-Fi-based SlimeVR trackers is **battery life** and **latency**: IBIS trackers run 50+ hours per charge and have lower lag, at the cost of needing a USB receiver instead of joining your home Wi-Fi.

## What the trackers do not do

A tracker only measures **rotation**, not absolute position. SlimeVR figures out position by chaining rotations together using your body proportions (your hip is below the headset, the upper leg pivots from there, the lower leg pivots from the knee, and so on). This is why **mounting calibration** and **body proportions** matter so much — get those right and tracking is rock solid.

This is also why drift happens over time: small rotation errors accumulate. That's what **reset bindings** are for — they tell the server "this is my new neutral pose, recalibrate."

## What the receiver does

The receiver is a small USB dongle with its own nRF radio. It listens for traffic from every paired tracker, deduplicates and timestamps the packets, and forwards them to the SlimeVR Server over USB. There's nothing for you to configure on it; it's plug-and-play.

The extension cable is **not optional**. The receiver's antenna is short, and 2.4 GHz is easily attenuated by your PC chassis. Extending it up and out of the case can double or triple your effective range.

## Where SlimeVR comes in

We didn't invent the protocol. IBIS trackers are SlimeVR-compatible, meaning they work with the official **SlimeVR Server** software maintained by the SlimeVR project. The server is open-source. For deep-dive technical material (IMU calibration internals, sensor fusion math, AutoBone), the [SlimeVR docs](https://docs.slimevr.dev) are the canonical reference.

Our docs cover the parts that matter for getting your IBIS trackers up and running. Anything below that layer, we'll happily link out.
