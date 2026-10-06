---
layout: post
title: "GTFS on the ground: auditing bus stops and transit infrastructure"
date: 2026-03-10 09:00:00 -0500
author: The OpenRoad Team
tags: [GTFS]
excerpt: "GTFS describes where transit is supposed to be. OpenRoad helps you check that against what's actually built on the street — shelters, signs, curb ramps, and stop locations."
---

**[GTFS]({{ site.gtfs_url }})** — the General Transit Feed Specification — is how the world publishes transit. It powers trip planners, arrival predictions, and countless maps. It's excellent at describing the *scheduled* system: routes, stops, and the times a bus should be there.

What GTFS doesn't tell you is what the stop physically looks like. Is there a shelter? A sign? A bench? A safe way to reach it? Does the marked stop location still match where the bus actually pulls over after a repaving project shifted the curb?

## The schedule vs. the sidewalk

Transit infrastructure drifts from its record just like everything else on the road:

- A stop is relocated for construction and the feed lags behind.
- A shelter is removed and never noted.
- A "stop" in the feed is really a pole with no accessible landing.
- Two nearby stops get consolidated, but both still appear.

These gaps matter most for the riders who depend on transit and can least afford a missing curb ramp or an unreachable stop.

## Checking it with OpenRoad

Load a **GTFS** feed as one of OpenRoad's inventory inputs and process a trip along the route. The app compares scheduled stops and transit infrastructure against what the trip actually captured — flagging stops that look different from the record, or locations where the physical stop and the feed disagree.

You review each observation with a swipe, map the confirmed ones, and export the result as open data an agency or advocate can act on. It's a lightweight way to keep the gap between the **schedule and the sidewalk** small — and to build an evidence base for where transit access needs investment.
