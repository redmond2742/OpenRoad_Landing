---
layout: post
title: "What is GTSS? Signal visibility and sight distance"
date: 2026-02-24 09:00:00 -0500
author: The OpenRoad Team
tags: [GTSS]
excerpt: "A look at how OpenRoad uses GTSS-style data to evaluate whether traffic signals are actually visible along an approach — and why sight distance is easy to lose and hard to catch."
---

A traffic signal only works if drivers can see it in time to react. That sounds obvious, yet signal visibility quietly degrades all the time — a tree grows into the sight line, a truck parks in the wrong spot, a new billboard competes for attention, or the approach grade hides the heads until it's almost too late.

**GTSS** data describes signals and their approaches in a structured way, and OpenRoad uses it to evaluate **signal visibility and sight distance**: is the signal visible far enough back along the approach for a driver traveling at the posted speed to stop or proceed safely?

## Why sight distance is tricky

Sight distance is a geometry problem tangled up with the real world:

- **Speed** sets how much stopping distance a driver needs, which sets how far back the signal must be visible.
- **Heading and grade** determine the line of sight along the approach.
- **Obstructions** — vegetation, parked vehicles, signs, structures — can block that line for only part of the year or part of the day.

A plan set says the signal is visible. A drive-through in July, with the trees leafed out, might say otherwise.

## Where OpenRoad fits

OpenRoad collects exactly the streams this analysis needs: **video** to see what the driver sees, **GPS** to locate it, **speed** to reason about stopping distance, and **heading** to reconstruct the approach. Processing a trip against GTSS-style data surfaces approaches where the signal may not be visible soon enough — as **observations** you then confirm in the swipe review step.

<div class="callout">
  <p>The point isn't to replace an engineering study. It's to flag candidate locations from real trips, so studies get pointed where they'll matter most.</p>
</div>

Because results export as [GeoJSON]({{ '/app/' | relative_url }}), a set of flagged approaches can go straight into a GIS for a signals engineer to review. And when [multiple drivers]({{ '/blog/2026/03/24/citizen-science-and-the-road/' | relative_url }}) flag the same intersection, that's a much stronger signal than one report alone.
