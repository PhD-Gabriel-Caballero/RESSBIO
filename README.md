# RESSBIO: REmote Sensing Spectroscopy for wetlands BIOdiversity

![Albufera_CHL_map](https://github.com/Grcf2585/RESSBIO/assets/92304222/3a65f864-e0dc-4327-8201-d2a18a9c4b88)

The [water ecological parameters jupyter notebook](https://github.com/Grcf2585/RESSBIO/blob/main/S2_water_index.ipynb) is an open-source code developed in Python that runs on Google Colab to interpret and compare chlorophyll, phycocyanin, and Secchi disk depth time series data obtained from retrieval models based on S2 multispectral data. Two retrieval strategies are implemented in the jupyter notebook: Gaussian Process Regression (GPR) and Parametric Indices (PI). The [GPR models](https://github.com/Grcf2585/RESSBIO/tree/main/Models) were trained and developed within the [ARTMO](https://artmotoolbox.com/) processing framework and then exported to be scalable in the Google Earth Engine cloud computing platform. The PI models were implemented using the following methodologies: 

+ [Chlorophyll](https://www.limnetica.com/es/monitoring-ecological-state-hypertrophic-lake-albufera-val%C3%A8ncia-spain-using-multitemporal-sentinel-2)
+ [Phycocyanyn](https://www.sciencedirect.com/science/article/pii/S0048969719342949?via%3Dihub)
+ [Secchi Disc Depth](https://www.limnetica.com/es/monitoring-water-transparency-hypertrophic-lake-albufera-val%C3%A8ncia-using-multitemporal-sentinel-2)

The models have been trained with [in-situ data](https://github.com/Grcf2585/RESSBIO/tree/main/In%20situ%20data) collected from several water reservoirs in Spain. The main authors are Gabriel Caballero, and Javier Soria-Perpina as part of the [Image Processing Laboratory](https://ipl.uv.es/?q=es) at the University of Valencia.

For a comprehensive overview of field campaigns and on-site data acquisition, see the [ESAQS](https://leoipl.uv.es/esaqs/) project webpage.

## Description
This repository contains the source codes for inland water ecological parameters retrieval through GEE using Python. This Google Colab application makes use of the [geemap](https://geemap.org/) Python package to interactively map with [Google Earth Engine](https://earthengine.google.com/), which is a cloud computing platform with a multi-petabyte catalogue of satellite imagery and geospatial datasets. The application takes the S2 multispectral data from the [COPERNICUS/S2_SR_HARMONIZED](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED) GEE image collection and applies the GPR and PI water parameter retrieval models to them. Although the study is focused on the Albufera of Valencia lagoon, users can configure any region of interest worldwide. We used the GEE technology to easily access the S2 data cubes and plot dense time series of water parameters data. 

Some of the challenges you faced and features you hope to implement in the future.

