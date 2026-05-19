---
title: FAQ
description: Common questions about VYRO-VR IBIS trackers.
---

## How do IBIS trackers connect to my PC?

Through the **USB receiver dongle** included with your kit. They do not use Wi-Fi. Plug the receiver into your PC, power on the trackers, and they appear in the SlimeVR Server within seconds. See [How the Trackers Work](/getting-started/how-trackers-work/).

## Wi-Fi trackers vs IBIS / NRF — what's the difference?

Standard SlimeVR Wi-Fi trackers join your home Wi-Fi network. IBIS trackers use a dedicated 2.4 GHz protocol via the receiver. Trade-offs:

- IBIS: 50+ hour battery life, lower latency, no Wi-Fi setup, requires receiver
- Wi-Fi: shorter battery life, requires 2.4 GHz Wi-Fi, no receiver needed

For most users, IBIS is the simpler and longer-lasting choice.

## Can I mix IBIS trackers with other SlimeVR trackers?

Yes. The SlimeVR Server treats all trackers equally — you can have IBIS trackers, official SlimeVR Wi-Fi trackers, and even Vive/Tundra trackers all running in the same session.

## Will IBIS work with my Quest?

**With a PC:** yes. Quest Link, Air Link, Virtual Desktop, or a cable — your Quest sees SlimeVR through SteamVR like any PCVR headset.

**Standalone Quest** (no PC at all): IBIS still requires a PC to run the SlimeVR Server and the receiver. The PC bridges to your headset over OSC. See [SteamVR & OSC](/slimevr-server/steamvr-and-osc/).

## How long does the battery last?

**50+ hours per charge** in normal use. Trackers auto-sleep after 15 minutes of inactivity, so a forgotten tracker won't drain overnight as long as you didn't bump it.

## How accurate is the tracking?

For full-body VR purposes — VRChat, dancing, exercise, social — IBIS tracking is excellent. Latency is low, drift is gentle, and Stay Aligned handles yaw drift automatically.

For sub-millimeter scientific measurement — no, IBIS is not the right tool. Use lighthouse-based systems (Vive trackers, Tundra Trackers) for that.

## How often do I need to calibrate?

- **Mounting calibration:** once per session at most. Often not at all if straps stayed in place from the last session.
- **Body proportions:** once, when you set up. Re-do if you significantly change shoes or weight.
- **Full reset:** every session start, plus occasionally during play.
- **Yaw reset:** as needed; with Stay Aligned, rarely.

## Are IBIS trackers waterproof?

**No.** They are not rated waterproof or even water-resistant. Don't wear them in the shower, swimming, or out in heavy rain. Sweat is generally fine — wipe trackers down after intense sessions.

## Can I update the firmware?

Yes — see [Updating Firmware](/firmware/updating/). It's optional; most users never need to.

## Do I need to be on Wi-Fi for the trackers to work?

**No.** The trackers and receiver are entirely self-contained. SlimeVR Server runs locally on your PC. The only network thing that requires internet is the very first download of the SlimeVR Server.

## Are IBIS trackers SlimeVR-compatible?

Yes. IBIS trackers run on the SlimeVR open-source protocol and are supported by the official SlimeVR Server software.

## Where can I get a replacement strap / dock / receiver?

[vyrovr.com](https://vyrovr.com) for new orders. For warranty or replacement of a defective part, reach out via [support](/support/).

## Can I buy a single tracker as a spare?

Yes — search "Single SlimeVR Compatible IBIS Tracker" at [vyrovr.com](https://vyrovr.com).

## What if I have a question not covered here?

[Discord](https://discord.gg/vyrovr) is the fastest path. We try to answer every question and feed back common ones to this site.
