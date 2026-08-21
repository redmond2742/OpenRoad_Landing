---
layout: default
title: About OpenRoad
description: "OpenRoad's mission: connect the data agencies already have with what people actually observe in the field, as structured, mapped, open roadway data."
permalink: /about/
body_class: page-about
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">Our mission</p>
    <h1 class="page-hero__title">Connecting agency data with what people see on the road</h1>
    <p class="page-hero__subtitle">
      Agencies hold a lot of roadway data. People on the road see a lot more. OpenRoad exists to close the
      gap between the two — as structured, mapped, open data.
    </p>
  </div>
</section>

<div class="container page-body prose" markdown="1">

## The gap we're closing

Transportation agencies maintain rich datasets: signal inventories, transit schedules, sign and marking catalogs, GIS layers of their networks. These describe how the system is *supposed* to be.

Out on the road, reality drifts. A signal gets occluded by a growing tree. A crosswalk fades. A new pothole opens after a hard winter. A bus stop moves. The official record and the physical world slowly diverge — and the people who notice first are the ones traveling those roads every day.

**OpenRoad connects existing agency data with what people actually observe in the field.** It takes the inventories that already exist — GTSS, GTFS, GIS/GeoJSON, CSV — and lets anyone with an iPhone check them against the ground truth of an ordinary trip.

## More than a road inspection app

It would be easy to describe OpenRoad as a road inspection tool. It's more than that. It's a **platform for turning field observations into structured, mapped, open roadway data** — usable whether you're a public works department, a transit agency, a university lab, an advocacy group, or a single resident who wants their street documented.

That framing shapes every design choice:

- **Structured**, so observations are consistent and analyzable, not scattered notes.
- **Mapped**, so every observation carries geographic context.
- **Open**, so data exports as GeoJSON and other formats anyone can use.

## Why open data

Roadway conditions are a shared concern, and the data about them shouldn't be trapped. Open formats mean an observation collected by a volunteer can be reviewed by an agency, analyzed by a researcher, and acted on by a maintenance crew — without conversion headaches or vendor lock-in.

## Stronger together: the crowd signal

A single report is easy to overlook. But when **multiple people** travel the same corridors and record what they see, their observations reinforce one another. Repeated observations from multiple users create **stronger crowd signals** — helping agencies identify locations that may need further review or improvement, backed by more than one voice.

<div class="callout">
  <p>OpenRoad doesn't replace professional inspection or agency judgment. It gives everyone — drivers, cyclists, pedestrians, volunteers, and advocates — a way to contribute credible, structured evidence to the conversation.</p>
</div>

## Where we're headed

We're building OpenRoad in the open, and writing about the ideas behind it — GTSS and sight distance, GTFS and transit infrastructure, dashcams as sensors, bike data collection, pavement sensing, and open roadway data. You can follow along on the <a href="{{ '/blog/' | relative_url }}">blog</a>.

</div>

{% include cta.html
   title="Help map the real state of the road"
   text="OpenRoad turns your everyday trips into open data that agencies and communities can use."
   secondary_label="Read the blog"
   secondary_url="/blog/" %}
