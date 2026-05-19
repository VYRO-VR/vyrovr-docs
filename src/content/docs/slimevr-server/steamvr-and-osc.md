---
title: SteamVR & OSC
description: Get your trackers into PCVR games (SteamVR) or standalone Quest/Pico (OSC).
---

There are two ways your IBIS trackers reach a game: through **SteamVR** (for PCVR) or **OSC** (for standalone headsets running compatible games like VRChat).

## SteamVR (PCVR)

If you play VR through a PC — Index, Vive, Quest Link / Air Link, Quest cable, Pimax, Bigscreen Beyond, etc. — you're using SteamVR.

### Setup

1. **Install the SlimeVR Server** ([Install](/slimevr-server/install/)). The installer automatically registers the SlimeVR SteamVR driver.
2. **Launch SlimeVR Server** before launching SteamVR (order doesn't strictly matter, but this is the reliable habit).
3. **Launch SteamVR.** Your trackers appear automatically as virtual Vive-style trackers.

### Confirming it worked

In the SteamVR status window, you'll see one entry per SlimeVR tracker (alongside your headset and controllers). They should all be **green / connected**.

In SteamVR's **Manage Trackers** panel, you can name each tracker by body part — but the SlimeVR Server already does this internally, so this step is optional.

### When SteamVR doesn't see them

See [Trackers Not Showing in SteamVR](/troubleshooting/steamvr-not-showing/).

## OSC (Quest standalone, Pico, etc.)

If you play standalone on a Quest or Pico without a PC, you can still use IBIS trackers via **OSC**, which is what VRChat-on-Quest accepts.

### The setup

- The trackers and the receiver still plug into a **PC on the same network** as your headset
- The SlimeVR Server runs on the PC
- The server broadcasts tracker data over OSC to the headset's IP address

### Configure

1. Find your headset's IP address (in VRChat: Settings → OSC → check the listening address)
2. In SlimeVR Server, open **Settings → OSC → VRChat**. Toggle on, paste in the headset IP, set the port (default 9000).
3. In VRChat on the headset, enable OSC trackers in Settings.
4. Re-launch VRChat. You'll now have trackers in your standalone session.

### Notes

- OSC only works in apps that support it. VRChat is the big one. Many other apps do not.
- Latency on standalone-via-OSC is higher than PCVR. Acceptable for VRChat, not great for competitive rhythm games.

For deeper OSC docs and edge cases, see the upstream [SlimeVR OSC page](https://docs.slimevr.dev/server/osc-information.html).
