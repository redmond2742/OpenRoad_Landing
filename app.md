---
layout: default
title: The OpenRoad App
description: "How the OpenRoad iOS app collects, processes, reviews, maps, and exports roadway data from everyday trips."
permalink: /app/
body_class: page-app
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">iOS app</p>
    <h1 class="page-hero__title">Every trip becomes structured roadway data</h1>
    <p class="page-hero__subtitle">
      OpenRoad runs on the iPhone you already carry. Start a trip and it records the road; finish it and
      you have data you can process, review, map, and export.
    </p>
    <p style="margin-top:1.2rem">
      {% include app-button.html %}
    </p>
  </div>
</section>

<section class="section map-band">
  <div class="container">
    <div class="section__head">
      <p class="eyebrow">Screens</p>
      <h2 class="section__title">From a moving trip to mapped, exportable data</h2>
      <p class="section__lead">A real look at OpenRoad on iPhone — processing a trip into taggable observations, reviewing them, and mapping the result.</p>
    </div>
    <div class="screenshots">
      {% include image.html src=site.images.app_process alt="OpenRoad's Process screen listing batches of sight-distance, signal, and asset photos ready to tag" caption="Process" %}
      {% include image.html src=site.images.app_review alt="Reviewing a sight-distance photo with swipe controls for Clear, Obstructed, and Unknown" caption="Review" %}
      {% include image.html src=site.images.app_map alt="Confirmed observations mapped across a corridor, filtered by Clear and Obstructed" caption="Map" %}
      {% include image.html src=site.images.app_detects alt="OpenRoad's list of what it detects: signal sight distance, rough pavement, roadside assets, transit stops, and more" caption="What it detects" %}
    </div>
  </div>
</section>

<div class="container page-body prose" markdown="1">

## Collect: sensor-rich capture

When you start a trip, OpenRoad records several streams at once, time-aligned so they can be analyzed together:

- **Video** — a forward view of the roadway from your iPhone camera.
- **GPS** — position and track, placing everything in geographic space.
- **Speed** — how fast you were traveling at each point.
- **Heading** — the direction of travel, useful for approach and sight-line analysis.
- **Accelerometer** — motion and vibration, the basis for detecting pavement and roadway condition events.

No special hardware is required. A phone mount and a normal drive, ride, or walk are enough to start building a dataset.

## Process: work with the data you already have

Raw sensor streams become useful when they're compared against known references. OpenRoad processes trips using **existing inventory files** rather than asking you to start from a blank slate:

- **[GTSS]({{ site.gtss_url }})** — evaluate signal visibility and sight distance along an approach.
- **[GTFS]({{ site.gtfs_url }})** — check bus stops and transit infrastructure against what's on the ground.
- **GIS / GeoJSON** — align trips to routes and geographic infrastructure layers.
- **CSV asset inventories** — bring in signs, markings, crosswalks, streetlights, and other static assets.

Processing surfaces **observations** — places along your trip where something is worth a closer look, whether that's a missing sign, an obstructed signal, or a rough stretch of pavement.

## Review: a simple swipe interface

Automated processing proposes; a person decides. OpenRoad presents observations one at a time in a fast **swipe interface** — confirm what's real, dismiss what isn't, and add context where it helps. Keeping a human in the loop means the data you export reflects judgment, not just a model's guess.

<div class="callout">
  <p><strong>Why review matters.</strong> Field conditions are messy — glare, occlusion, and edge cases are common. A quick human confirmation step turns noisy candidates into trustworthy records.</p>
</div>

## Map: see results in context

Confirmed observations are placed on a map, linked to the roads and assets they describe. Mapping makes patterns visible — clusters of condition events, corridors with repeated signage issues, or gaps between an inventory and reality.

## Export: open formats, ready to use

Finished data leaves OpenRoad in open, interoperable formats — **GeoJSON** and others — so it drops straight into GIS tools, agency systems, and analysis pipelines. Nothing is locked in a proprietary silo; your observations are yours to share and build on.

</div>

{% include workflow.html
   heading="One pipeline, end to end"
   lead="The same five steps power every trip in OpenRoad." %}

{% include supported-data.html %}

{% include cta.html
   title="Ready to record your first trip?"
   text="Get OpenRoad for iPhone and turn the road in front of you into open data."
   secondary_label="Build an asset CSV"
   secondary_url="/csv-builder/" %}
