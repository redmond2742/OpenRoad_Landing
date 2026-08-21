---
layout: post
title: "Dashcams as sensors: video is data, not just footage"
date: 2026-04-14 09:00:00 -0500
author: The OpenRoad Team
tags: [dashcams]
excerpt: "A dashcam records what happened. OpenRoad treats the same forward-facing video as a sensor stream — time-aligned with GPS, speed, and heading so it can become structured roadway data."
---

Most people think of a dashcam as an insurance device: a camera that quietly records the road so there's footage if something goes wrong. That's useful, but it treats video as a passive archive.

OpenRoad treats the same forward-facing video as a **sensor**.

## What changes when video is a sensor

Footage becomes data when it's tied to everything else you know about the moment it was captured:

- **GPS** anchors each frame to a location.
- **Speed** tells you how fast the scene was moving past.
- **Heading** tells you which way the camera — and the driver's attention — was pointed.
- **Accelerometer** marks the jolts and events worth revisiting.

With those streams time-aligned, a stretch of video stops being "a clip" and becomes a georeferenced record of the roadway: the signs that passed, the signals ahead, the condition of the pavement, the state of a crosswalk.

## Why the phone is enough

You don't need a dedicated dashcam. A modern iPhone captures high-quality video and carries the GPS, motion, and orientation sensors OpenRoad needs, all in one device with a good clock to keep them in sync. That's the whole reason the app can turn an **everyday trip** into structured data without new hardware.

## From clip to record

In OpenRoad, the video feeds the **Process** step, where it's compared against your inventory files, and the **Review** step, where you confirm observations. What comes out the other end isn't footage sitting on an SD card — it's [open, mapped data]({{ '/app/' | relative_url }}) you can export and share.

The dashcam was always collecting information. OpenRoad just makes that information usable.
