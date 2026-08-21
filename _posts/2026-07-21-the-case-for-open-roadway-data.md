---
layout: post
title: "The case for open roadway data"
date: 2026-07-21 09:00:00 -0500
author: The OpenRoad Team
tags: [open data]
excerpt: "Why OpenRoad exports GeoJSON and other open formats by default — and how open roadway data lets a volunteer's observation reach a maintenance crew without friction."
---

Every design decision in OpenRoad points toward one outcome: data that leaves the app in **open, interoperable formats**. That's not an afterthought. It's the reason the app exists.

## What "open" buys you

A roadway observation is only valuable if it can reach the people who can act on it. Open formats remove the friction between them:

- A **volunteer** records a faded crosswalk on a walk.
- The observation is confirmed in review and mapped.
- It exports as **GeoJSON**, a format any GIS can read.
- An **agency** loads it alongside their own layers.
- A **maintenance crew** gets a work location, and a **researcher** can analyze the pattern across a city.

No proprietary export step, no vendor lock-in, no "please request a data extract." The path from observation to action is short because the format is open.

## Interoperability is the whole point

OpenRoad is deliberately built around formats that already exist across the field:

- **GTSS** for signals and sight distance
- **GTFS** for transit infrastructure
- **GIS / GeoJSON** for routes and geographic layers
- **CSV** for static asset inventories

Reading these on the way in and writing open data on the way out means OpenRoad **connects** systems rather than competing with them. Your observations slot into the tools you and your partners already use.

## Trust through openness

Open data is also more trustworthy data. When the output is a standard file anyone can inspect, there's nothing hidden in a black box. Observations are structured, geolocated, and reviewable — and because they're portable, they can be corroborated by [multiple contributors]({{ '/blog/2026/03/24/citizen-science-and-the-road/' | relative_url }}) rather than trapped in one person's account.

That's the platform we're building: not another silo of road data, but a way to turn field observations into structured, mapped, **open** roadway data that moves freely to wherever it's needed.
