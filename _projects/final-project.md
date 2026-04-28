---
layout: project
title: "Iowa Business & Population Analysis"
description: "Business activity across Iowa counties with population context."
image: /assets/pngs/final_project_preview.png
importance: 1
category: IS445
tags: [Python, Altair, Vega-Lite]
---

## Overview

**Author:** Hemangi Sanjay Chaudhari  

This project explores retail business registrations in Iowa and how they relate to county population. It combines an interactive dashboard with supporting visualizations to provide both trends and context.

---

## Interactive Dashboard

<div id="vis"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed('#vis', "/assets/json/final_dashboard.json");
</script>

**Description**  
This dashboard compares active and inactive businesses and shows how registrations have changed over time. Active businesses are higher overall, and there is a clear increase after 2015. Users can click on a business status to filter the trend and explore patterns more clearly.

---

## Top Counties by Business Registrations

<div id="vis2"></div>

<script>
vegaEmbed('#vis2', "/assets/json/context_business_count.json");
</script>

**Description**  
This chart highlights the counties with the highest number of business registrations. Polk County stands out, followed by Linn and Scott. The color encoding represents population, showing that more populated counties tend to have more businesses.

---

## Top Counties by Population

<div id="vis3"></div>

<script>
vegaEmbed('#vis3', "/assets/json/context_population.json");
</script>

**Description**  
This chart shows the most populated counties in Iowa. Polk County has the highest population, which aligns with its high number of business registrations. This suggests that population size influences business activity.

---

## Interactivity

The dashboard includes interactive filtering. Selecting a category (Active or Inactive) updates the time-series chart, allowing users to explore trends dynamically. Tooltips also provide detailed values when hovering over the charts.

---

## Data & Methods

[The Data](/assets/data/iowa_retail_business_registrations_sample.csv)  
[Cleaned Population Data](/assets/data/iowa_county_population.csv)  
[The Analysis](/python_notebooks/final_project.ipynb)
