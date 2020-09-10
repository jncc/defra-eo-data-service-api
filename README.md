# defra-eo-data-service-api
These two Jupyter Notebooks download Sentinel 2 satellite images from DEFRA EO data service.

# eods-api-generate-cloudless-mosaic.ipynb
First run this Notebook which downloads a list of all the Sentinel 2 images that are in the Area of interest defined within the Notebook. These are saved as two csv files that are used in the EODS_API Notebook. Also, the username and token proved by the DEFRA EO website must be entered in the config.py script so the Notebook can use them
to download the list of images. 

# EODS_API.ipynb
This Notebook downloads the list of Sentinel 2 satellite images using the two csv created in the previous Notebook. Additionally, this Notebook will also create a mosaic of the downloaded images, mask them using a shapefile and finally calculate the NDVI of the clipped image. 

For this notebook to work correctly the RSGISLIB library package, (https://www.rsgislib.org/) for Jupyter Notebook is needed. 
To make a conda install of this follow the instructions below:

In Anaconda prompt:

1. Create the conda environment and install the two libraries needed (rsgislib and Jupyter) with:

$ conda create --name rsgislibenv -c conda-forge rsgislib jupyter
 
2. activate the environment you just created with:

$ conda activate rsgislibenv
 
3. start the Jupyter notebook server which should launch in a browser or give the localhost URL:

$ jupyter notebook


