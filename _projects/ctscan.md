---
name: CT Scan Visualization
tools: [Python, Altair, Vega-Lite]
description: Interactive CT scan visualizations.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# CT Scan Visualizations

Some explanation of the data here.

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz1_intensity_profile.json" style="width: 100%"></vegachart>

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz2_slice_viewer.json" style="width: 100%"></vegachart>

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/single_dicom.h5" text="the data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Jerulor/jerulor.github.io/blob/main/python_notebooks/vis1.ipynb" text="the analysis" %}
</div>
