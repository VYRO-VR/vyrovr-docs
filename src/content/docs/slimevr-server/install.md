---
title: Install SlimeVR Server
description: Download and install the SlimeVR Server on your PC.
---

The **SlimeVR Server** is the open-source desktop app that drives your IBIS trackers. It's free, made by the SlimeVR project, and required.

## Windows (most users)

1. Go to [slimevr.dev](https://slimevr.dev).
2. Download the **SlimeVR Installer**.
3. Run the installer. It bundles the server, the GUI, the SteamVR driver, and the Java runtime — there's nothing else to install.
4. Launch **SlimeVR Server** from the Start menu when it's done.

On first launch, Windows may prompt about firewall access — **allow both Private and Public networks**. The server needs to talk to its GUI even on PCs without external networking.

## macOS

The Windows installer doesn't work on macOS. Follow the [SlimeVR macOS install guide](https://docs.slimevr.dev/tools/MacOS-Installation.html). VYRO VR does not test against macOS internally; PCVR on Mac is unusual.

## Linux

See the [SlimeVR Linux install guide](https://docs.slimevr.dev/tools/linux-installation.html). Most PCVR-on-Linux users are on SteamVR with Proton, and the standard Linux server build works fine.

## What got installed

After install you'll have:

- **SlimeVR Server** — the background app that talks to your trackers (this is what to launch)
- **SlimeVR GUI** — the window the server opens (you don't launch it separately)
- **SteamVR driver** — auto-registers; SteamVR sees your trackers automatically once it's running
- **A few support binaries** — firmware tools, etc.

## Updating

The server checks for updates on launch and prompts you when a new version is out. Update through the prompt; don't run the installer over the top unless you're recovering from a broken install.

## Uninstalling

Standard Add/Remove Programs on Windows. The SteamVR driver is removed with the rest. No leftovers if you reinstall later.
