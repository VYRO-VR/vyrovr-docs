---
title: Installing the Receiver
description: Plug in your USB receiver dongle and confirm it's recognized.
---

The receiver is the small USB stick that talks to your trackers. It's the only piece of hardware besides the trackers that has to be connected to your PC.

:::caution[Always use the extension cable]
**Do not plug the receiver directly into your PC.** The receiver is small and its USB connector is fragile — repeatedly plugging it straight into a PC port (especially the back of a tower) can damage the connector. The included USB extension cable protects the receiver **and** dramatically improves wireless range. Use it every time.
:::

## Step by step

1. **Plug the receiver into the USB extension cable**, not directly into your PC.
2. **Plug the other end of the extension cable** into a free USB port on your PC. Any USB-A port works; USB 2.0 is fine.
3. **Place the receiver up and away** from your computer — clipped to a shelf, taped to the back of a monitor, hanging from a desk lamp, whatever works. Higher = better. See [Range & Placement](/receiver/range-and-placement/) for why this matters.
4. **Plug in a tracker** (single button press to power on). It should appear in the SlimeVR Server window within a few seconds.

That's it. No drivers, no pairing app, no Wi-Fi credentials. The receiver is HID-class and Windows / macOS / Linux all recognize it without setup.

## How do I know it's recognized?

- On Windows, Device Manager will show a HID-compliant device appearing when you plug the receiver in.
- In the SlimeVR Server window, any powered-on paired tracker will show up. If the SlimeVR Server window shows zero trackers and you know your trackers are charged, the receiver is the likely suspect — see [Receiver Not Detected](/troubleshooting/receiver-not-detected/).

## Do not

- Plug the receiver directly into the back of a tower PC. The metal chassis kills 2.4 GHz range — that's literally what the extension is for.
- Plug it into a USB 3.0 hub near your headset cable. USB 3 emits 2.4 GHz noise; co-locating the receiver with USB-3 traffic causes dropouts.
- Bend the receiver's body. The internal antenna is short — let the extension cable do the routing.

## Multiple receivers

Each receiver works as a single, self-contained pairing group. You can run two receivers (e.g., one VYRO VR kit + one borrowed setup) on the same PC if you really want to, but trackers paired to receiver A will not appear via receiver B. For everyday use, one receiver per playspace is the answer.
