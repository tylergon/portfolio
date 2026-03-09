---
title: "Post-Fire Recovery: Analyzing the 2017 Prouton Lakes Fire"
meta_title: ""
description: "Analyzing the severity of the Prouton Lakes fire and subsequent recovery"
date: 2025-12-07
image: "/images/fire-severity.png"
categories: ["Geomatics", "Wildfire"]
author: "N. Tyler Goncalves"
tags: ["Geomatics", "Wildfire"]
draft: false
---

For this project, I was evaluating the fire severity and subsequent vegetative recovery of the 2017 Prouton Lakes fire, located within the Alex Fraser Research Forest (AFRF) in British Columbia. I tracked the landscape's transformation from 2013 to 2021 using a time-series remote sensing approach.

### Methodology: Time-Series Analysis

To quantify both the immediate and long-term regeneration, I used Landsat imagery to calculate two primary spectral indices:

- **Normalized Difference Vegetation Index (NDVI):** Used primarily to track greenness and biomass recovery post-fire.
- **Normalized Burn Ratio (NBR):** Leveraged to identify burned areas and calculate the Differenced Noramlized Burn Ratio (dNBR) for severity classification.

### Analysis & Severity Classification

The heart of the study was developing a time-series analysis to compare pre-fire baselines (2013-2016) against the immediate post-fire environment and the four-year recovery window.

1. **Severity Mapping:** By calculating the dNBR between 2016 and 2017, I classified the burn into levels (unburned, low, medium, high severity). This provided a spatial distribution of where the fire intensity was most destructive within the AFRF.

2. **Statistical Trends:** I developed charts to visualize the average NDVI and NBR fluctuations across the entire area. These charts clearly show the dive in NDVI in 2017 and the gradual upward slope of the recovery seen in the following years.

### Learning Outcomes

This project was a dive into the temporal aspects of geomatics, seeing how powerful the deep archives of Landsat are to analyze changes in the landscape due to natural disasters. The data clearly shows the long-term impact of the fires: the landscape still holds telltales signs of the fire and is working its way back towards its baselines. I'd be interested to push this exploration a bit further, perhaps through analysis with a higher resolution data source or by looking for trends in how the topography impacted the wildfires path. Stay tuned for more!