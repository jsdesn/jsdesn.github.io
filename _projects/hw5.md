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

For this vizualization, I created a bar chart that displays the total number of UFO sightings across the US states. This plot uses a Nominal(N) encoding for the state variable on the X-axis and a Quantitative (Q) encoding for the count of sightings on the Y-axis.

To make the graph look better I chose to sort the states in descending order based on the number of sightings and applied a viridis color scheme, which maps the magnitude of sightings to a perceptually uniform color scale, which makes it easier to identify sates with high report volumes like California. I used Pandas to filter the raw dataset for US-based entries and performed a groupby to aggregate the sightings.
### Visualization 2: Time of Day vs. Duration

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

This graph is a scatter plot shoing the relationship between the time of day a sighting occurs and how long it lasts. This chart uses a Temporal(T) encoding for the X-axis and a Quantitative(Q) encoding for the Y-axis. The shape of the UFO is represented as a Nominal (N) variable using a discrete color scheme to differentiate between categories like 'disk' or 'light'.

For interactivity, I used a selection interval that lets users click and drag across the plot to highlight specific clusters of data. This allows users to isolate specific times frames or duration ranges to see which shapes are the most common. I converted the datetime strings into python datetime objects to allow for proper temporal scaling and filtered the duration data to remove extreme outliers, which ensures the majority of the data porints are visible without excessive compression of y-axis.

## Search The Data & Methods


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jsdesn/jsdesn.github.io/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

