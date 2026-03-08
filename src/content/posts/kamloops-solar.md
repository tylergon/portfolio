---
title: "An Open-Source Workflow for Evaluating Rooftop Solar Potential"
meta_title: ""
description: "My capstone project developing an open source workflow for evaluating rooftop solar potential using Kamloops as a case study"
date: 2026-03-06
image: "/images/kamloops_insolation.png"
categories: ["Geomatics", "Energy"]
author: "N. Tyler Goncalves"
tags: ["Geomatics", "Energy"]
draft: false
---

For my Master's capstone project, I hoped to develop an open-source workflow capable of predicting rooftop solar potential using only ALS and meteorological data. Given BC's goal to develop a province-wide inventory of ALS, this would have massive potential for evaluating the potential of a province-wide distributed solar power system.

---

### Methods

The analysis broke down into four major stages, optimized for the massive scale of citywide ALS. 

Processing an entire city's worth of ALS data at a high resolution is a huge challenge. To circumvent computational and temporal restrictions, I performed the analysis on a neigbhourhood-by-neighbourhood basis. This choice let me process the city in a reasonable amount of time while still chunking the site in a format that would be useful for municipal decisionmakers down the line.

#### Data Acquisition & Preprocessing

The methods only require two data inputs: (1) 2024 ALS collected and provided by the City of Kamloops, (2) meteorological data from the CWEC (Canadian Weather Year for Energy Calculation) database.

#### Building Footprint Identification

Using the lidR package in R, I normalized the point cloud and applied classification and height filters to remove non-building points below 2.5m. The remaining points were rasterized at a 2m spatial resolution. To isolate individual structures, I used Rook's Case adjacency clustering.

#### Solar Irradiation Simulation

I used the UMEP SEBE (Solar Energy on Building Envelopes) plugin within QGIS. By using a Digital Surface Model (DSM) of building and ground points, and a Canopy Height Model (CHM), the model simulated annual solar radiation across all roof surfaces, accounting for shading and atmospheric effects.

#### Suitability Analysis

To narrow the analysis down to surfaces able to feasibly support solar panel installation:

1. **Slope:** Eliminating rooftops too steep for installation.
2. **Aspect:** Remove north-facing orientations.
3. **Building Size:** Minimum building area requirements.
4. **Insolation Thresholds:** Eliminating areas that did not economically support solar PV.

---

This project was an excellent experience. For starters, it allowed me to pursue a project that was an inspiration for my studies in geomatics: modelling the potential of rooftop solar. It also gave me the opportunity to work with data on a scale I've never gotten the chance to experience, which held a number of learning opportunities regarding processing efficiency and big-data management. 

Down the line, I'm excited to revisit the project to try to build on the existing code, perhaps by adding in obstacle identification or automated solar panel fitting. But this was only the beginning, soon I'm looking to take this past Kamloops and apply it to cities all around BC.