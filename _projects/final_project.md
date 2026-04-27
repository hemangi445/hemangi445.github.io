---
layout: project
title: "Iowa Business Registrations Dashboard"
---

## Overview
This visualization explores retail business registrations in Iowa. It allows users to compare active and inactive businesses and observe how they have changed over time.

## Interactive Dashboard
<div id="vis"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script type="text/javascript">
  var spec = "/assets/json/final_dashboard.json";
  vegaEmbed('#vis', spec);
</script>
