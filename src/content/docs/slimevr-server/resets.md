---
title: Resets
description: Full reset, yaw reset, mounting reset — what they do and how to bind them.
---

Trackers drift. Not a lot, but enough that after 20-30 minutes of play, your virtual feet might be facing slightly to the side of your real feet. **Resets** fix that.

## The three resets

### Full reset

Re-zeros **all** tracker rotations to your current pose. Stand straight, face forward, trigger it. Everything snaps back to neutral.

Use when: drift has built up, or after a session pause where you sat down and got back up.

### Yaw reset

Re-zeros only **horizontal rotation** (left/right facing). Faster, less invasive than a full reset — useful as a "just fix my heading" tweak.

Use when: your avatar is facing slightly off but vertical alignment (feet on the floor, etc.) feels fine.

### Mounting reset

Re-runs **mounting calibration** for all trackers. Use if a tracker shifted on your body or you put it on the wrong way around mid-session.

Use when: one specific tracker is acting weird and you don't want to take the headset off.

## Binding resets

By default, you trigger resets from the SlimeVR Server window. That's fine for setup, but in VR you need them bound to **controller buttons** or **keyboard shortcuts**.

### SteamVR bindings (PCVR users)

1. Start SteamVR.
2. SteamVR menu → **Devices** → **Controller bindings** → pick your controller → **SlimeVR**.
3. Bind a button (long-press or chord) to **Full reset**.
4. Bind another to **Yaw reset**.
5. Optionally bind **Mounting reset** to a longer chord.

Common bindings: hold-the-system-button + thumbstick click, or a double-tap of a face button.

### Keyboard / Feeder App

If you're on Quest standalone or want hotkeys for SteamVR, the SlimeVR **Feeder App** lets you bind keyboard shortcuts. Defaults are Ctrl+Alt+Shift combinations. See the Feeder App settings inside the SlimeVR window.

## Reset etiquette

- Stand straight when you trigger a full reset
- Face the direction you want to be "forward"
- Don't trigger a reset mid-motion — you'll zero against a weird pose

## How often should I reset?

- **Yaw reset:** every 5-10 minutes is normal for most users; bind it to an easy button
- **Full reset:** once per session start, then as needed
- **Mounting reset:** rarely — only if something feels actively wrong

If you find yourself yaw-resetting constantly, try **Stay Aligned** (server 0.16+) — it auto-corrects yaw drift while you play. See [Stay Aligned](/firmware/stay-aligned/).
