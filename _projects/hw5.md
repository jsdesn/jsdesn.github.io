---
name: Homework 5 visulaizations
tools: [Python, HTML]
image: 
description: This is a "showcase" for the vizualizations made for hw5
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# UFO Sightings Visualizations

This is the [dataset](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv) that was used.

### Visualization 1: Sightings by State

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>

This bar chart visualizes the distribution of UFO sightings across different US states. I chose to use a **Nominal (N)** encoding for the states on the X-axis and a **Quantitative (Q)** encoding for the count of sightings on the Y-axis. To make the data more readable, I sorted the states in descending order of sightings and applied a 'viridis' color scheme to highlight the density of reports. In my Python notebook, I transformed the data by filtering for US-based reports and aggregating the total counts per state using a groupby operation to ensure the resulting JSON file remained lightweight for web hosting.

### Visualization 2: Time of Day vs. Duration

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

The second visualization is a scatter plot examining the relationship between the time of day a sighting occurred and the duration of that encounter. I utilized a **Temporal (T)** encoding for the time (hours) and a **Quantitative (Q)** encoding for the duration in seconds. The color is mapped to the UFO shape, which is a **Nominal (N)** variable. For interactivity, I implemented a **selection interval (brush)**; this allows users to highlight specific clusters of sightings by clicking and dragging, which helps in identifying patterns among different shapes or specific times of night. On the analysis side, I converted the raw datetime strings into Python datetime objects and filtered out extreme duration outliers to maintain a clear visual scale.

## Search The Data & Methods


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jsdesn/jsdesn.github.io/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

