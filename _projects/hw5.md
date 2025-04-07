---
title: "Bigfoot Sightings Visualization"
excerpt: "An interactive exploration of Bigfoot sightings across the U.S., using Altair and Vega-Lite."
collection: projects
image: /assets/pngs/map_thumb.png
tags:
  - Python
  - HTML
  - altair
  - vega-lite
---

## HW5: Bigfoot Sightings Visualization

This page presents two visualizations created using Python + Altair based on the BFRO Bigfoot sightings dataset.

---

### 📍 Plot 1: Sightings by Location

<iframe src="/assets/plots/map_plot.html" width="700" height="500"></iframe>

**Description**: This map visualizes the geographic distribution of Bigfoot sightings across the United States. Each circle represents a sighting, with its color showing the classification (Class A, B, or C). Class A sightings are blue, Class B are orange, and Class C are black.

**Design choices**: Longitude and latitude were used as positional encodings. Color encodes the classification, with distinct colors chosen to maximize contrast. Tooltips were added for the state, date, and season of each sighting.

**Transformations**: Date parsing and missing value removal were done. The `date` column was converted to datetime, and entries missing key spatial or temporal data were dropped.

---

### 📅 Plot 2: Sightings Over Time (Interactive)

<iframe src="/assets/plots/bar_plot.html" width="700" height="500"></iframe>

**Description**: This bar chart shows the number of Bigfoot sightings over time, broken down by season. The user can filter by state using a dropdown menu to explore patterns over time in different regions.

**Design choices**: The x-axis shows the year (as an ordinal), and the y-axis encodes the count of sightings. Color encodes season. The dropdown menu allows filtering the chart by state, improving the clarity of temporal trends by region.

**Transformations**: The `year` column was derived from the parsed `date`. Missing years were excluded.

**Interactivity**: The dropdown filter allows users to explore how Bigfoot sightings vary over time by state, making trends easier to analyze and more engaging.

---

### 🔗 Links

- [🔗 The Data (CSV)](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv)  
- [📓 The Notebook (GitHub)](https://github.com/srighini/srighini.github.io/blob/main/python_notebooks/bigfoot_viz.ipynb)
