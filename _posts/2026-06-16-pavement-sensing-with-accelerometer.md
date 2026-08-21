---
layout: post
title: "Pavement sensing: reading the road through the accelerometer"
date: 2026-06-16 09:00:00 -0500
author: The OpenRoad Team
tags: [pavement sensing]
excerpt: "The accelerometer in your phone feels every pothole, joint, and rough patch. Here's how OpenRoad turns that motion into geolocated roadway condition events."
---

You can hear and feel bad pavement before you can describe it — the drone of a coarse surface, the bang of a pothole, the rhythmic thud of failing joints. Your phone feels it too. The **accelerometer** that counts your steps and rotates your screen is sensitive enough to register the vibration and shock of the road passing beneath a vehicle.

OpenRoad uses that signal to detect **pavement and roadway condition events**.

## From motion to events

Raw accelerometer data is a busy stream of numbers. The useful part is the departures from normal:

- A sharp spike is a **pothole** or a hard edge.
- Sustained high-frequency vibration is a **rough or degraded surface**.
- Periodic jolts are often **joints or cracking** at regular intervals.

Paired with **GPS**, each of these becomes a **geolocated condition event** — not just "the road is rough somewhere" but "a jolt occurred here, at this speed, on this heading."

## Why speed and context matter

The same bump feels different at 20 mph and 55 mph, and a heavy vehicle transmits it differently than a light one. That's why OpenRoad records **speed** and **heading** alongside the motion data, and why the **Review** step keeps a human in the loop: automated detection proposes condition events, and a person confirms which ones are real before they become records.

<div class="callout">
  <p>Pavement sensing from phones won't replace a formal pavement condition survey. It will tell you where to send one — cheaply, continuously, and from trips people are already taking.</p>
</div>

## Continuous, crowd-scale monitoring

The real promise is coverage. Formal pavement surveys are periodic and expensive. Phone-based sensing is continuous and nearly free once people are driving with the app. When [many trips]({{ '/blog/2026/03/24/citizen-science-and-the-road/' | relative_url }}) cross the same segment, repeated condition events at the same spot become a strong signal — exported as [open data]({{ '/app/' | relative_url }}) a maintenance team can prioritize.
