---
layout: post
title: "Introducing OpenRoad: your drive, recorded as data"
date: 2026-02-10 09:00:00 -0500
author: The OpenRoad Team
tags: [development]
excerpt: "Why we're building an iOS app that turns everyday trips into structured, mapped, open roadway data — and how the Collect, Process, Review, Map, Export pipeline came together."
---

Roads are measured constantly, but the measurements are scattered. An agency has a signal inventory in one system, a sign catalog in another, transit schedules in a third, and a GIS layer that's mostly right. Meanwhile, the people who actually travel those roads — every day, in every condition — carry a device packed with sensors and see problems the official record misses.

OpenRoad started from a simple question: **what if an ordinary trip could become structured data?**

## The pipeline

We kept coming back to five steps, and they became the backbone of the app:

1. **Collect** — record video, GPS, speed, heading, and accelerometer data from an iPhone.
2. **Process** — compare that trip against existing inventory files (GTSS, GTFS, GIS/GeoJSON, CSV).
3. **Review** — confirm or dismiss observations with a fast swipe interface.
4. **Map** — place confirmed observations in geographic context.
5. **Export** — output GeoJSON and other open formats.

Each step is deliberately boring in the best way. Nothing here requires special hardware, a proprietary cloud, or a data science team. A phone mount and a normal drive are enough to start.

## Not just inspection

The easy pitch is "a road inspection app." We think that undersells it. OpenRoad is a **platform for turning field observations into structured, mapped, open roadway data**. Inspection is one use. So is citizen science, transit auditing, pavement monitoring, and building an inventory where none existed.

## What's next

Over the coming posts we'll dig into the specific data OpenRoad understands — starting with [GTSS and signal sight distance]({{ '/blog/2026/02/24/what-is-gtss/' | relative_url }}) — and the ideas that shape the app: dashcams as sensors, bike data collection, pavement sensing, and why open roadway data matters. Follow along, and if you want to see the workflow in detail, read about [the app]({{ '/app/' | relative_url }}).
