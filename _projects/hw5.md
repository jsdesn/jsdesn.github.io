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

The first graph shows the total UFO sightings by US states.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>

The secound graph shows the sightings based on seasonality and duration.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

## Search The Data & Methods


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/assets/json/UFO.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jsdesn/jsdesn.github.io/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

