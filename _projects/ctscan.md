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

{% raw %}
<vegachart schema-url="{{ site.baseurl }}/assets/json/viz1_intensity_profile.json" style="width: 100%"></vegachart>
{% endraw %}

{% raw %}
<vegachart schema-url="{{ site.baseurl }}/assets/json/viz2_slice_viewer.json" style="width: 100%"></vegachart>
{% endraw %}

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/single_dicom.h5" text="the data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/python_notebooks/ct_scan_visualizations.ipynb" text="the analysis" %}
</div>
