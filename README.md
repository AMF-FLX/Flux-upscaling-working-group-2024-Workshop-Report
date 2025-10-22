# Flux-upscaling-working-group-2024-Workshop-Report
Flux upscaling working group / 2024 Workshop Report: Remote Sensing and Fluxes Upscaling for Real-world Impact

## Introduction

Understanding and scaling land-atmosphere fluxes remains one of the final frontiers in Earth system science. While flux networks like AmeriFlux and NEON have matured into cornerstones for in situ monitoring, spatial integration with remote sensing and modeling still lacks systematic workflows and common standards. This is especially the case for supporting practical applications in agriculture, forestry, and urban planning.  
To address this challenge, we established the Flux Upscaling Working Group, led by members of AmeriFlux Management Project, NEON, and the Carbon Dew Community of Practice, to bring together experts and advance the integration of flux and remote sensing data. Our goal is to develop a novel framework and define best practices that facilitate the effective use of these data sources.  
The "Remote Sensing and Fluxes Upscaling for Real-world Impact" workshop brought together experts from various fields to discuss and address the challenges of integrating remote sensing and flux data across different spatiotemporal scales. 

## 2024 Remote Sensing and Fluxes Upscaling for Real-world Impact workshop
This repository contains materials from the 2024 Remote Sensing and Fluxes Upscaling for Real-world Impact workshop focused on analyzing and integrating remote sensing and flux data using Jupyter Notebooks. The workshop featured a series of presentations, which are outlined in the agenda included in this repository. 

The repository is organized as follows:
- **Hands-on Tutorial**: A collection of Jupyter notebooks providing tutorials and examples for working with remote sensing and flux data, designed to be run on Google Colab.
- **Presentations**: The workshop presentations, including slides and supporting materials, are presented in accordance with the agenda. The available slides are from speakers who have granted permission to make their material publicly available. 

To run the notebooks, simply open them in Google Colab and follow the instructions. This repository aims to provide a resource for participants and others interested in learning about remote sensing and flux data analysis and integration.

### External Resorces 
- Datasets created and used in the hands-on session can be also found [here](https://drive.google.com/file/d/1WyAYDHvut789H-oEbO6Lm-ObKP1wlbM5/view?usp=sharing).
- Recordings of the sessions are available on the [event](https://go.lbl.gov/vy35rp) page of the Ameriflux web portal.  

## Workshop Steering Committee
Nicola Falco (Lawrence Berkeley National Laboratory)  
Koong Yi (Lawrence Berkeley National Laboratory)  
Stefan Metzger (AtmoFacts, Carbon Dew Community of Practice)  
David Durden (National Ecological Observatory Network)  
Chris Florian (National Ecological Observatory Network)  
Paul Stoy (Univ. of Wisconsin-Madison)  
Mallory Barnes (Indiana University)  
Gavin McNicol (Univ. of Illinois Chicago)  

## Coordinator
Christin Buechner (Lawrence Berkeley National Laboratory)

# Hands-on Tutorial
## Topic 1: From site-scale ...   
Creators: Micola Falco (nicolafalco@lbl.gov), David Durden (ddurden@battelleecology.org), Stefan Metzger (smetzger@atmofacts.com)

This topic focuses on site-scale analysis using remote sensing (RS) data. We will:
- Collect RS data using Google Earth Engine (GEE) and Colab (Python API)
- Process the data using practical codes, covering key steps such as:
    - Calculating vegetation indices
    - Visualizing data as maps
    - Extracting time-series information
    - Conducting quality assessment (QA)
    - Comparing RS time-series with tower flux data (Net Ecosystem Exchange, NEE)
    - Aggregating RS and flux time-series data
    - Modeling the relationship between vegetation indices and NEE using a linear model.

See [License](https://github.com/AMF-FLX/Flux-upscaling-working-group-2024-Workshop-Report/blob/main/LICENSE) and [COPYRIGHT](https://github.com/AMF-FLX/Flux-upscaling-working-group-2024-Workshop-Report/blob/main/COPYRIGHT) files for licensing details and copyright details.

## Topic 2: ... over regional-scale connectivity ...
Creators: Micola Falco (nicolafalco@lbl.gov), David Durden (ddurden@battelleecology.org), Stefan Metzger (smetzger@atmofacts.com)  

In Topic 2 of this tutorial, we will explore regional-scale connectivity by:
- Applying the linear model developed in Topic 1 to estimate Net Ecosystem Exchange (NEE) over a small region, using a straightforward analysis approach
- Utilizing high-frequency flux spatialization to investigate additional factors influencing NEE in space, time, and process.

See [License](https://github.com/AMF-FLX/Flux-upscaling-working-group-2024-Workshop-Report/blob/main/LICENSE) and [COPYRIGHT](https://github.com/AMF-FLX/Flux-upscaling-working-group-2024-Workshop-Report/blob/main/COPYRIGHT) files for licensing details and copyright details.

## Topic 3: ... to continental-scale connectivity
Creators: Danielle Losos (losos@wisc.edu), Paul Stoy (pcstoy@wisc.edu), Sophie Hoffman (shoffman22@wisc.edu), Sadegh Ranjbar (sranjbar@wisc.edu), Ryan Abernathey (ryan@earthmover.io)  

In Topic 3, we will scale up to continental connectivity by introducing the Baseline Imager Live Imaging of Vegetated Ecosystems (ALIVE) workflow, specifically ALIVE-GPP. This lesson will cover:
-Leveraging data from the Advanced Baseline Imager on Geostationary Operational Environmental Satellites - R Series (GOES-R) for pixels containing Ameriflux and NEON towers
-Using a machine learning model to estimate Gross Primary Productivity (GPP) at a 5-minute temporal resolution, matching the ABI CONUS scene
-Working with zarr libraries created using Arraylake by earthmover, specifically a library containing GPP estimates.

# Acknowledgement

