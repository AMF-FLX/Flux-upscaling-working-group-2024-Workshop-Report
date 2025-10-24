# Flux-upscaling-working-group-2024-Workshop-Report
Flux upscaling working group / 2024 Workshop Report: Remote Sensing and Fluxes Upscaling for Real-world Impact

## Introduction

Understanding and scaling land-atmosphere fluxes remains one of the final frontiers in Earth system science. While flux networks like AmeriFlux and NEON have matured into cornerstones for in situ monitoring, spatial integration with remote sensing and modeling still lacks systematic workflows and common standards. This is especially the case for supporting practical applications in agriculture, forestry, and urban planning.  
To address this challenge, the Flux Upscaling Working Group, led by members of AmeriFlux Management Project, NEON, and the Carbon Dew Community of Practice, brings together experts to advance the integration of flux and remote sensing data with the goal of developing a novel framework and define best practices that facilitate the effective use of these data sources.  
The "Remote Sensing and Fluxes Upscaling for Real-world Impact" workshop was held in June 2024 at the Berkeley Lab, Ca. It brought together experts from various fields to discuss and address the challenges of integrating remote sensing and flux data across different spatiotemporal scales and applications. 

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
Creators: Danielle Losos (losos@wisc.edu), Paul Stoy (pcstoy@wisc.edu), Avanti Kekane (avkekane@wisc.edu), Sophie Hoffman (shoffman22@wisc.edu), Sadegh Ranjbar (sranjbar@wisc.edu), Ryan Abernathey (ryan@earthmover.io)

In Topic 3, we will scale up to continental connectivity by introducing the Advanced Baseline Imager Live Imaging of Vegetated Ecosystems ([ALIVE](https://alive-abi.github.io/alive/index.html)) workflow that we call 'ALIVE<sub>GPP</sub>', also described in this [google slides presentation](https://docs.google.com/presentation/d/1PJclqluGFHkp9LpHZ85_pgL8lFLLaAMsQcEGZ2DIGSU/edit#slide=id.p1) that was created for the workshop.

The tutorial will cover:
- How to work with [zarr](https://zarr.dev/) libraries created using [Icechunk](https://icechunk.io/en/latest/overview/#docs-organization) by [earthmover](https://earthmover.io/). We will use a zarr library that contains [Gross Primary Productivity (GPP) estimates](https://alive-abi.github.io/alive/daily-GPP.html) from the ALIVE worksflow.
- Leveraging data from the [Advanced Baseline Imager](https://www.goes-r.gov/spacesegment/abi.html) on the [Geostationary Operational Environmental Satellites - R Series (GOES-R)](https://www.goes-r.gov/) to create ALIVE<sub>GPP</sub> for pixels that contain Ameriflux and NEON, Inc. towers as described in [Losos et al. (2024)](https://www.nature.com/articles/s41597-024-03071-z)
- Using a machine learning model specifically a gradient boosting model described in [Ranjbar et al. (2024)](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2024MS004341), to estimate GPP at the native temporal resolution of the ABI CONUS scene, every 5 minutes, as described in [Losos et al. (2025)](https://www.sciencedirect.com/science/article/pii/S0034425725001634).

# Acknowledgments

This tutorial was developed using resources and data from various sources. If you use this tutorial or modify it for your own research or educational purposes, please acknowledge the original repository and contributors.

To acknowledge this repository, please cite it as follows:

### Topic 1 and 2:
- Falco, Nicola, Metzger, Stefan, and Durden, David. 2024 Workshop - Remote Sensing and Fluxes Upscaling for Real-world Impact - Tutorial v1. Computer Software. https://github.com/AMF-FLX/Flux-upscaling-working-group-2024-Workshop-Report. USDOE. 14 Apr. 2025. Web. doi:10.11578/dc.20251024.5.

### Topic 3:
- Losos, D., Hoffman, S. & Stoy, P.C. GOES-R land surface products at Western Hemisphere eddy covariance tower locations. Sci Data 11, 277 (2024). https://doi.org/10.1038/s41597-024-03071-z
- Ranjbar, S., Losos, D., Hoffman, S., Cuntz, M., & Stoy, P. C. (2024). Using geostationary satellite observations and machine learning models to estimate ecosystem carbon uptake and respiration at half hourly time steps at eddy covariance sites. Journal of Advances in Modeling Earth Systems, 16, e2024MS004341. https://doi.org/10.1029/2024MS004341
- Losos, D., Ranjbar, S., Hoffman, S., Abernathey, R., Desai, A. R., Otkin, J., Zhang, H., Ryu, Y., & Stoy, P. C. (2025). Rapid changes in terrestrial carbon dioxide uptake captured in near-real time from a geostationary satellite: The ALIVE framework. Remote Sensing of Environment, 324, 114759. https://doi.org/10.1016/j.rse.2025.114759

By acknowledging this repository and its contributors, you help to promote transparency, reproducibility, and recognition of the work that has gone into creating this resource.


