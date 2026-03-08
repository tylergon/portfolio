---
title: "Modelling Grizzly Bear Connectivity in the Rockies"
meta_title: ""
description: ""
date: 2026-03-06
image: "/images/grizzly-bear-lcp.png"
categories: ["Geomatics", "Energy"]
author: "N. Tyler Goncalves"
tags: ["Geomatics", "Energy"]
draft: false
---

For this project, I assumed the role of a conservation analyst to understand movement corridors for Grizzly Bears in Western Alberta. Using geospatial data to model and pretict the suitable habitat and movement corridors for these animals is critical for conservation efforts as human activity continues to fragment their historical range.

### The Workflow

To prepare the data, I used GDAL to rasterize the study area. Given the large size of the study area, using a command line tool like GDAL should be significantly more efficient than using its GUI-based counterparts. It worked perfectly, and with my love for open-source, I'm interested in exploring this tool more, so I'll be trying to work it into my workflow whenever I can going forward.

##### Constructing the Cost Surface

To understand how a Grizzly moves across the landscape required defining the "cost" of movement: what biological and physical resistance does a bear experience? Using a variety of data sources, I synthesized the following 3 variables into a cost surface:

1. **Land Cover:** Assigning a higher cost to urbanized or open areas where a bear may avoid, and lower costs to dense forest cover.
2. **Topography (Slope):** Steep terrain represents a higher physical tax on the animal's movement.
3. **Human Proximity (Roads):** Using roads both as a proxy for human activity and to quantify the risk associated with crossing transportation corridors.

##### Distance Accumulation

Using ArcGIS Pro, I performed a distance accumulation analysis. This type of analysis calculates the accumulated cost a bear would experience over time as it treks across the great expanse of the Rockies.

Using a randomly generated start and end point across the Rocky Mountain foothills, the model calculated a Least Coss Path representing the mathematically optimal route a bear would take to minimize energy expenditure and human contact while maximizing the use of preferred habitat. 

### Key Takeaways

This lab highlighted the importance of developing skills that cross technological barriers. While ArcGIS has a built in, sophisticated suite of tools, GDAL provides a low overhead, efficient, reproducable method for preparing data. More importantly, it was an excellent introduction into understanding how geomatics could be used to provide quantitative analysis for conservation, such as determining the most suitable locations for wildlife overpasses or identifying critical patches of habitat for migration.