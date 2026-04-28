---
name: Iowa Business & Population Analysis
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/final_project_preview.png
description: Business registrations across Iowa counties and how they relate to population.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

**Author: Hemangi Sanjay Chaudhari**

---

## Overview

This project explores how many businesses are registered across different counties in Iowa and how those numbers relate to population. The first visualization is an interactive dashboard that compares active and inactive businesses and shows how registrations have changed over time. The next two visualizations provide more context by showing which counties have the highest number of registered businesses and how population might explain those patterns.

---

## Active vs Inactive Businesses and Registration Trends

<br>

<vegachart schema-url="{{ site.baseurl }}/assets/json/final_dashboard.json" style="width: 70%; margin: auto;"></vegachart>

<br>

This interactive dashboard shows the difference between active and inactive businesses in Iowa and how business registrations have changed over time. The bar chart compares the total number of active and inactive businesses, while the line chart shows how registrations change year by year. Color is used to clearly separate business status, and position is used to represent the number of businesses. The date column was cleaned and converted into a year format in Python so that the trend over time could be displayed clearly. Users can click on a business status (Active or Inactive) to filter the line chart. This helps them focus on one category at a time and better understand how registrations change.

---

## Top Iowa Counties by Business Registrations

<br>

<vegachart schema-url="{{ site.baseurl }}/assets/json/context_business_count.json" style="width: 80%; margin: auto;"></vegachart>

<br>

This chart shows the top 15 counties in Iowa based on the number of registered businesses. A horizontal bar chart is used because it makes county names easier to read. The length of each bar represents the number of businesses, and color represents population. This makes it easier to see that counties with larger populations tend to have more businesses. Polk County stands out as having the highest number of registered businesses.

---

## Top Iowa Counties by Population

<br>

<vegachart schema-url="{{ site.baseurl }}/assets/json/context_population.json" style="width: 80%; margin: auto;"></vegachart>

<br>

This chart shows the top 15 counties in Iowa by population. It helps explain the results from the previous chart by showing that counties with higher populations also tend to have more registered businesses. Counties like Polk and Linn appear at the top in both charts. The simple bar chart design makes it easy to compare population across counties.

---

## Interactivity

The dashboard includes interactive filtering. When a user clicks on a business status, the line chart updates to show trends only for that category. This makes the visualization more useful because users can explore the data in more detail instead of viewing everything at once. Tooltips also appear when hovering over the charts to show exact values.

---

## Sources

The visualizations in this project were created by the author using the following datasets:

- [Iowa Retail Business Registrations dataset](https://catalog.data.gov/dataset/retail-sales-and-retail-use-business-registrations?from_hint=eyJxIjoicmV0YWlsIHNhbGVzIiwic29ydCI6InJlbGV2YW5jZSJ9)

- [U.S. Census population dataset](https://data.census.gov/table?q=B01003&g=040XX00US19%240500000)

All data cleaning, processing, and visualizations were performed by the author using Python (pandas) and Altair.

---

## Search The Data & Methods

<br>

<div style="display: flex; justify-content: space-between; margin-top: 30px; margin-bottom: 30px;">
  <div>
    {% include elements/button.html link="https://github.com/hemangi445/hemangi445.github.io/blob/main/assets/data/iowa_retail_business_registrations_sample.csv" text="The Data" %}
  </div>

  <div>
    {% include elements/button.html link="https://github.com/hemangi445/hemangi445.github.io/blob/main/python_notebooks/final_project.ipynb" text="The Analysis" %}
  </div>
</div>

<br>
