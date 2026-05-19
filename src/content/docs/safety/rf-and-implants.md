---
title: RF & Medical Implants
description: 2.4 GHz radio safety, particularly around pacemakers and implanted devices.
---

IBIS trackers transmit on **2.4 GHz** at low power, the same frequency band as Wi-Fi, Bluetooth, and your microwave oven. The radio output is in the same range as a typical Bluetooth headset — small.

For nearly all users, there is nothing to think about. The notes below are for users with **active implanted medical devices** (pacemakers, defibrillators, neurostimulators, insulin pumps, and similar).

## Implanted medical devices

The general guidance from device manufacturers is to keep wireless transmitters **at least 15 cm (6 inches)** away from the implanted device.

Practically, for IBIS:

- **Chest tracker** (sternum, via the chest harness) — this is the closest tracker to common pacemaker placements (upper-left chest). **If you have a pacemaker or ICD in this area, consult your cardiologist before using a chest tracker.** Lower-body tracking without a chest tracker is fine.
- **Other trackers** (legs, arms) — meet the 15 cm rule by definition during normal wear.

## What the trackers emit

- Frequency: **2.4 GHz** (proprietary protocol, not Wi-Fi or BLE)
- Output power: low (consumer ISM-band, comparable to BLE peripherals)
- Duty cycle: continuous broadcasts at packet rate while powered on

Continuous low-power radio operation has been studied extensively in the BLE / Wi-Fi / 802.15 context. No mechanism is known to cause harm at these power levels. If you're skeptical of consumer radios in general, the chest tracker is the variable to drop.

## Interference

Distinct from health concerns: 2.4 GHz devices in close proximity can interfere with each other. Things that share the band:

- Wi-Fi (especially 2.4 GHz Wi-Fi)
- Bluetooth headsets, mice, keyboards
- Microwave ovens
- Other VR tracking systems

This is a **performance** topic, not a safety topic. See [Range & Placement](/receiver/range-and-placement/) if your tracking is dropping out.

## Pregnancy

IBIS trackers emit RF comparable to a Bluetooth headset or a smartphone. We don't have specific guidance to offer beyond "talk to your healthcare provider if you'd like to be cautious." Many pregnant users continue using VR comfortably; consult your own provider.

## If in doubt

Ask your medical professional. The relevant facts to share with them: 2.4 GHz proprietary radio, low-power ISM band, intermittent transmission, peripheral wearable. We're happy to provide more specifics on the radio module if your provider asks — reach out via [support](/support/).
