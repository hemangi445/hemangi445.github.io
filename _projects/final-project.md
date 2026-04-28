---
name: Iowa Business & Population Analysis
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/final_project_preview.png
description: Business activity across Iowa counties with population context.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

## Overview

**Author:** Hemangi Sanjay Chaudhari  

This project explores Iowa retail business registrations and county population data. The first visualization is an interactive dashboard that compares active and inactive businesses and shows how registrations changed over time. The second and third visualizations add population context by comparing top counties by business registrations and population.

## Visualization 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/final_dashboard.json" style="width: 100%"></vegachart>

This interactive dashboard compares active and inactive businesses in Iowa. The bar chart shows the total number of businesses by status, and the line chart shows how registrations changed over time. I used position to encode the count of businesses and color to separate active and inactive businesses. I also converted the permit issue date into a year column in Python so the yearly trend could be plotted clearly.

## Visualization 2

<vegachart schema-url="{{ site.baseurl }}/assets/json/context_business_count.json" style="width: 100%"></vegachart>

This visualization shows the top 15 Iowa counties by business registrations. I used a horizontal bar chart because county names are easier to read this way. The x-axis shows the number of businesses, the y-axis shows county names, and color represents population. This helps show that counties with larger populations often have more business registrations.

## Visualization 3

<vegachart schema-url="{{ site.baseurl }}/assets/json/context_population.json" style="width: 100%"></vegachart>

This visualization shows the top 15 Iowa counties by population. This chart gives context for the business registration chart because population size can help explain why some counties have more businesses. Polk County has the highest population and also appears as the top county for business registrations.

## Interactivity

The first visualization includes interactivity. When a user selects Active or Inactive in the bar chart, the line chart updates to show the registration trend for that selected business status. This makes the dashboard more useful because the viewer can move from a general comparison to a more specific trend without needing separate charts.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://github.com/hemangi445/hemangi445.github.io/blob/main/assets/data/iowa_retail_business_registrations_sample.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/hemangi445/hemangi445.github.io/blob/main/python_notebooks/final_project.ipynb" text="The Analysis" %}
</div>
