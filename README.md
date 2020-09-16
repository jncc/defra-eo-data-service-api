
# Accessing Sentinel-2 satellite imagery via the Defra EO Data Service API
These Jupyter Notebooks were created to demonstrate how to access Sentinel-2 analysis-ready data (ARD) using the application programming interface (API) provided by the [Defra Earth Observation Data Service](https://defradigital.blog.gov.uk/2020/06/18/making-it-easier-to-access-and-use-earth-observation-data/).  The EO Data Service is available to members of staff at Defra, its agencies and arms length bodies.  In order to run these Notebooks, you need to know your username and authentication token for the EO Data Service and you will need to use a computer on your organisation's IT network.  

![Alt text](https://github.com/jncc/defra-eo-data-service-api/blob/master/CUU_Logos.png?raw=true "Optional Title")














# eods-api-generate-cloudless-mosaic.ipynb
This Notebook was produced by SCISYS (now part of [CGI](https://www.cgi-group.co.uk/en-gb)) on behalf of JNCC and Defra.
First run this Notebook which downloads a list of the Sentinel-2 images with the least cloud cover for the date range and area of interest defined within the Notebook. These lists are saved as two csv files that are used in the EODS_API Notebook. Please note that your username and authentication token for the Defra EO Data Service must be entered in the config.py script so the Notebook can use them to download the list of images. 

# Installing RSGISLib
For the next two notebooks to work correctly the [RSGISLib](https://www.rsgislib.org/) library package for Jupyter Notebook is needed. 

To make a conda install of this follow the instructions below:

In Anaconda prompt:

1. Create the conda environment and install the two libraries needed (rsgislib and Jupyter) with:

$ conda create --name rsgislibenv -c conda-forge rsgislib jupyter
 
2. activate the environment you just created with:

$ conda activate rsgislibenv
 
3. start the Jupyter notebook server which should launch in a browser or give the localhost URL:

$ jupyter notebook

# EODS_API.ipynb
This Notebook was produced by JNCC with funding from the Caroline Herschel Framework Partnership Agreement on [Copernicus User Uptake](https://jncc.gov.uk/our-work/copernicus-project/). 
This Notebook downloads Sentinel-2 satellite images using the two csv files created in the previous Notebook. Additionally, this Notebook will also create a mosaic of the downloaded images, clip them using a shapefile and finally calculate the NDVI of the clipped image. 


# EODS_API_Best_pixel.ipynb
This Notebook was produced by JNCC with funding from the Caroline Herschel Framework Partnership Agreement on [Copernicus User Uptake](https://jncc.gov.uk/our-work/copernicus-project/). 
This Notebook downloads Sentinel-2 satellite images using the two csv files created in the eods-api-generate-cloudless-mosaic.ipynb. It then creates a best-pixel composite using the pixels with the lowest cloud cover in a stack of imagery from different dates.









