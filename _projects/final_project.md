---
layout: project
title: "Iowa Business Registrations and Population"
description: "An interactive data story about Iowa retail business registrations and county population."
importance: 1
category: IS445
---

## Overview

This project explores retail business registrations in Iowa and compares them with county population. The goal is to understand where business activity is concentrated and whether larger counties also tend to have more business registrations.

## Interactive Dashboard

<div id="vis"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed('#vis', "/assets/json/final_dashboard.json");
</script>

This dashboard compares active and inactive businesses and shows how registrations changed over time. When a user clicks **Active** or **Inactive** in the bar chart, the line chart updates to show the trend for that selected business status. This makes it easier to move from a general summary to a more specific trend.

## Context Visualization 1

<div id="vis2"></div>

<script>
vegaEmbed('#vis2', "/assets/json/context_business_count.json");
</script>

This chart shows the top 15 Iowa counties by business registrations. Polk County has the highest number of business registrations, followed by Linn and Scott. The color also shows population, so the chart connects business activity with county size.

## Context Visualization 2

<div id="vis3"></div>

<script>
vegaEmbed('#vis3', "/assets/json/context_population.json");
</script>

This chart shows the top 15 Iowa counties by population. Polk County also has the highest population, which helps explain why it has the most business registrations. Comparing this chart with the business registration chart gives extra context for the story.

## Interactivity

The main dashboard includes interactive filtering. Selecting a business status in the first chart changes the trend chart on the right, so users can explore active and inactive businesses separately. The charts also include tooltips, so users can hover over marks to see exact values.

## Data & Methods

[The Data](/assets/data/iowa_retail_business_registrations_sample.csv)  
[Cleaned Population Data](/assets/data/iowa_county_population.csv)  
[The Analysis](/python_notebooks/final_project.ipynb)
