
<img align="right" width="175" height="85" src="https://github.com/Grcf2585/RESSBIO/assets/92304222/4fd0f098-ea32-457e-ae98-c5b7cfa78070">
<!<img align="left" width="250" height="125" src="https://github.com/Grcf2585/RESSBIO/assets/92304222/73954397-7fc9-497b-8258-02a086fa425d">

# RESSBIO: REmote Sensing Spectroscopy for wetlands BIOdiversity

[![geemap](https://img.shields.io/badge/Python%20%2B%20GEE-geemap-blue)](https://geemap.org/) [![ARTMO](https://img.shields.io/badge/GPR-ARTMO-green)](https://artmotoolbox.com/) [![S2 Collection](https://img.shields.io/badge/Optical%20data-Sentinel%202-orange)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED) <a href="https://studiolab.sagemaker.aws/import/https://github.com/Grcf2585/RESSBIO/blob/main/S2_water_index.ipynb">
  <img src="https://studiolab.sagemaker.aws/studiolab.svg" alt="Open In SageMaker Studio Lab"/>
</a>

![Albufera_CHL_map](https://github.com/Grcf2585/RESSBIO/assets/92304222/24c5c9b2-2c02-4d62-989b-4fa905b80920)
The [water ecological parameters jupyter notebook](https://github.com/Grcf2585/RESSBIO/blob/main/S2_water_index.ipynb) is an open-source code developed in Python that runs on Google Colab to interpret and compare chlorophyll, phycocyanin, and Secchi disk depth time series data obtained from retrieval models based on S2 multispectral data. Two retrieval strategies are implemented in the jupyter notebook: Gaussian Process Regression (GPR) and Parametric Indices (PI). The [GPR models](https://github.com/Grcf2585/RESSBIO/tree/main/Models) were trained and developed within the [ARTMO](https://artmotoolbox.com/) processing framework and then exported to be scalable in the Google Earth Engine cloud computing platform. The PI models were implemented using the following methodologies: 

+ [Chlorophyll](https://www.limnetica.com/es/monitoring-ecological-state-hypertrophic-lake-albufera-val%C3%A8ncia-spain-using-multitemporal-sentinel-2)
+ [Phycocyanyn](https://www.sciencedirect.com/science/article/pii/S0048969719342949?via%3Dihub)
+ [Secchi Disc Depth](https://www.limnetica.com/es/monitoring-water-transparency-hypertrophic-lake-albufera-val%C3%A8ncia-using-multitemporal-sentinel-2)

The models have been trained with [in-situ data](https://github.com/Grcf2585/RESSBIO/tree/main/In%20situ%20data) collected from several water reservoirs in Spain. The main authors are Gabriel Caballero, and Javier Soria-Perpina as part of the [Image Processing Laboratory](https://ipl.uv.es/?q=es) at the University of Valencia.

For a comprehensive overview of field campaigns and on-site data acquisition, see the [ESAQS](https://leoipl.uv.es/esaqs/) project webpage.
See [Tutorials & Examples](#item1) to get started.

## Description
This repository contains the source codes for inland water ecological parameters retrieval through GEE using Python. This Google Colab application makes use of the [geemap](https://geemap.org/) Python package to interactively map with [Google Earth Engine](https://earthengine.google.com/), which is a cloud computing platform with a multi-petabyte catalogue of satellite imagery and geospatial datasets. The application takes the S2 multispectral data from the [COPERNICUS/S2_SR_HARMONIZED](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED) GEE image collection and applies the GPR and PI water parameter retrieval models to them. Although the study is focused on the Albufera of Valencia lagoon, users can configure any region of interest worldwide. We used the GEE technology to easily access the S2 data cubes and plot dense time series of water parameters data. The time series tool allows applying and comparing the water ecological parameters evolution retrieved by GPR and PI models in eutrophic lagoons.  

## How to use the Project
This application requires authentication in GEE. You will need a GEE account to proceed. 
```ruby
try:
    ee.Initialize()
except Exception as e:
    ee.Authenticate()
    ee.Initialize()
```
A Google Drive is also necessary for saving project outputs. You must mount your Drive by indicating your Google e-mail account.  
```ruby
from google.colab import drive
drive.mount('/content/drive')
```
<a name="item1"></a>
## Tutorials & Examples

![CHL_time_series](https://github.com/Grcf2585/RESSBIO/assets/92304222/b5266955-da77-46b3-a7b0-b998a7ac1657)

![PC_time_series](https://github.com/Grcf2585/RESSBIO/assets/92304222/482d8a1f-e6a4-4f45-b0f7-cce064a62f3e)

![SDD_time_series](https://github.com/Grcf2585/RESSBIO/assets/92304222/8e29fcac-003b-491f-8c70-7ceb29af8f1e)

