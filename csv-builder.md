---
layout: default
title: Asset CSV Builder
description: "Create CSV inventories of static roadway assets — signs, markings, crosswalks, and streetlights — to process alongside your OpenRoad trips."
permalink: /csv-builder/
body_class: page-csv
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">Companion tool</p>
    <h1 class="page-hero__title">Asset CSV Builder</h1>
    <p class="page-hero__subtitle">
      A web app for building CSV inventories of static roadway assets — signs, markings, crosswalks,
      streetlights, and more — so OpenRoad can process your trips against them.
    </p>
  </div>
</section>

<div class="container page-body prose" markdown="1">

## Why a CSV of assets?

OpenRoad's **Process** step compares your trips against inventory files you already have. But not every agency or volunteer group starts with a clean GIS layer. The Asset CSV Builder gives you a simple way to create one: a plain **CSV inventory** of the static assets you care about, ready to load into OpenRoad.

Static assets are the fixed things along a corridor:

- **Signs** — regulatory, warning, and guide signs
- **Markings** — lane lines, stop bars, and symbols
- **Crosswalks** — marked pedestrian crossings
- **Streetlights** — lighting locations and coverage
- …and anything else you can describe as a point with attributes.

## How it fits the workflow

<div class="callout">
  <p><strong>Collect → Process → Review → Map → Export.</strong> The Asset CSV Builder feeds the <em>Process</em> step. Build your inventory once, then process any number of trips against it inside OpenRoad.</p>
</div>

Because the output is ordinary CSV, it's easy to edit, version, and share — and it works alongside the other formats OpenRoad understands, like GTSS, GTFS, and GIS/GeoJSON.

<div class="big-cta">
  <h2>Open the Asset CSV Builder</h2>
  <p class="lead">Create and download a CSV inventory in your browser, then load it into OpenRoad.</p>
  <p>
    {% assign csv = site.csv_builder_url %}
    {% if csv and csv != "" and csv != "#" %}
      <a class="btn btn--primary" href="{{ csv }}" target="_blank" rel="noopener">Launch the CSV Builder →</a>
    {% else %}
      <span class="btn btn--primary btn--disabled" aria-disabled="true">CSV Builder link coming soon</span>
    {% endif %}
  </p>
</div>

## What a simple inventory looks like

A CSV inventory is just rows of assets with a location and some attributes. For example:

```csv
id,type,latitude,longitude,notes
1,stop_sign,40.44210,-79.99530,faded
2,crosswalk,40.44255,-79.99612,unmarked north leg
3,streetlight,40.44301,-79.99688,out
```

You decide which columns matter for your project — the builder helps you produce a consistent file that OpenRoad can read.

</div>

{% include cta.html
   title="Pair your inventory with real trips"
   text="Build a CSV of static assets here, then record trips in OpenRoad and process them against it."
   secondary_label="How the app works"
   secondary_url="/app/" %}
