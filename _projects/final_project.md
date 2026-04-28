---
layout: project
title: "Iowa Business Registrations Dashboard"
---

## Overview
This project explores retail business registrations in Iowa and how they relate to population. It includes an interactive dashboard and additional charts to provide more context.

---

## Interactive Dashboard

<div id="vis"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed('#vis', "/assets/json/final_dashboard.json");
</script>

### Description
This dashboard compares active and inactive businesses and shows how registrations have changed over time. Active businesses are significantly higher, and there is a noticeable increase in registrations after 2015. The interaction allows users to explore trends more clearly.

---

## Top Counties by Business Registrations

<div id="vis2"></div>

<script>
vegaEmbed('#vis2', "/assets/json/context_business_count.json");
</script>

### Description
This chart highlights the counties with the highest number of business registrations. Polk County stands out, followed by Linn and Scott. The color shows population, indicating that higher population counties tend to have more businesses.

---

## Top Counties by Population

<div id="vis3"></div>

<script>
vegaEmbed('#vis3', "/assets/json/context_population.json");
</script>

### Description
This chart shows the most populated counties in Iowa. Polk County has the highest population, which aligns with its high number of business registrations. This suggests that population size influences business activity.
