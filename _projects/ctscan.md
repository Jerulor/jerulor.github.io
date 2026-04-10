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

### Visualization1: graph that goes through each slice in the ct scan and shows pixel intensity

This visualization is a simple graph that shows the clarity and resolution of each slice as you go from the top to bottom of the scan. To be honest, I got the ideas for each visualization from a friend in bio-medical engineering, and so while he tried to explain to me what a backprojection is and what exactly axial depth entails, I think the graph best shows which slices have a better resolution. 

because the CT scan is ordered and numbered, the encoding for this graph is quantitative; the data is meant to be displayed but also operated on to show averages, quantiles, and maximums, there's few operations to be done with it. I didn't really think about the color scheme, red dotted line for the top to show the maximum clarity in each slice, and heavy blue at the bottom to draw attention to the averages instead of the max. I thought the original graph looked very plain, so I asked AI to add the percentiles and the blue shading for the variance as well as to improve the formatting.

This graph isn't as interactive as i'd like it to be, but I do like how each slice has a point you can hover over to see the information instead of trying to line it up with the y-axis to see exact information. I think it's more interesting for the user to "zoom in" on each slice on their own as opposed to having a table displayed or a big report talking about each slice.

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz1_intensity_profile.json" style="width: 100%"></vegachart>

## Visualization 2: go through each layer of the ct scan with a slider

I'm a big fan of this type of graph, it's a graph that displays a slice in grayscale, but the slider allows the user to go through each slice in order, almost giving the experience of being the ct scan and going from top to bottom.

This graph is mostly ordinal, the data itself is ordinal as no operations are really to be done with it, they're just positions with which to display the slices. However the slider and the color scheme are quantitative, since they have to be operated with in order to display the greyscale and intensity of each pixel. I went with greyscale because it looks more medical, I've never gotten a teeth x-ray in color so it would be strange to display it in blue or red or some other hue. 

The interactivity in this graph comes from the slice slider. It reminds me of something you'd see in a museum in order to look through the different phases of an animal or a geological artifact. It's not very technically impressive but it's almost always a cool experience for the user to be able to flip through the images in order to create a 3d image in their mind of what the brain scan looks like.

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz2_slice_viewer.json" style="width: 100%"></vegachart>


<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/single_dicom.h5" text="the data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Jerulor/jerulor.github.io/blob/main/_projects/vis1.ipynb" text="the analysis" %}
</div>
