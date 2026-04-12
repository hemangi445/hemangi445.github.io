---
name: HW5 Data Visualization
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/cars.png
description: Two visualizations from one dataset for Homework 5
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

## Overview

This project explores the Illinois professional licenses dataset using two Altair visualizations. The first visualization highlights the most common license types and lets the viewer interactively inspect the license status distribution for a selected type. The second visualization shows how the number of records changes over time for the five most common license types.

## Visualization 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/hw5_plot1.json" style="width: 100%"></vegachart>

This visualization focuses on the top 10 most common license types in the dataset. The top chart uses horizontal bars to show record counts for each license type, which makes it easy to compare categories with long text labels. The bottom chart shows the distribution of license statuses for the selected license type. I used position to encode count and category, and color to separate categories more clearly. I filtered the dataset in Python to only the top 10 license types so the chart would stay readable and not become overcrowded.

## Visualization 2

<vegachart schema-url="{{ site.baseurl }}/assets/json/hw5_plot2.json" style="width: 100%"></vegachart>

This visualization shows the number of records over time for the top five license types using a line chart. A line chart works well here because the goal is to show change across years. The x-axis encodes effective year, the y-axis encodes the number of records, and color distinguishes the different license types. In the notebook, I converted the effective date column into a datetime format and created an effective year column so the yearly trend could be plotted more clearly.

## Interactivity

The first visualization includes interactivity. When a user selects a license type in the top chart, the bottom chart updates to show the license status breakdown for that selected type. This makes the visualization more useful because it allows the viewer to move from a general overview to a more specific breakdown without creating separate static charts.

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/hemangi445/hemangi445.github.io/blob/main/python_notebooks/hw5.ipynb" text="The Analysis" %}
</div>
