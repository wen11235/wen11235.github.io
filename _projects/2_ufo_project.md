---
name: UFO Sightings in the US
tools: [Python, HTML, Altair]
image: assets/pngs/ufo.png
description: This project visualizes UFO sightings across the United States over time and by reported shapes, with interactive elements.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
permalink: /projects/2-ufo-project/index.html
---

## HW5: UFO Sightings in the United States Visualization

This project presents two visualizations created using Python + Altair based on the BFRO Bigfoot sightings dataset.


---

##  Plot 1: UFO Sightings per Year

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufochart1.json" style="width: 100%"></vegachart>

**Description:**  
This line chart shows the number of UFO sightings per year after 1980. It visualizes how reports of sightings have changed over time, highlighting trends or potential spikes in UFO activity.

**Design Choices:**  
I used a line chart with the x-axis representing the year (as an ordinal variable) and the y-axis showing the number of sightings (quantitative). The line makes it easy to see trends over time.

**Transformations:**  
The original dataset included date and time strings. I converted the `datetime` column to `datetime` objects and then extracted the year using `dt.year`. I also dropped any rows where the year was missing or invalid.

---

## Plot 2: UFO Shapes by State (Interactive)

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufochart2.json" style="width: 100%"></vegachart>

**Description:**  
This interactive bar chart displays the number of UFO sightings by reported shape, filtered by U.S. state. Users can select a state from the dropdown to explore the most commonly reported shapes in that state.

**Design Choices:**  
I used a bar chart to represent shape frequency, with `shape` on the x-axis and count on the y-axis. The bars are color-coded by shape for clarity. A dropdown menu allows filtering by state, making the chart interactive.

**Transformations:**  
I removed rows with missing `shape` or `state` values.

**Interactivity:**

The dropdown menu that lets users explore how UFO shape reports vary across different U.S. states.

---

##  Data and Notebook
- [The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)  
- [The Analysis]( https://github.com/wen11235/wen11235.github.io/blob/main/python_notebooks/hw5-1.ipynb)

