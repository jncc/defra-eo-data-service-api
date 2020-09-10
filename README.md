# defra-eo-data-service-api
These two Jupyter Notebooks download Sentinel 2 sattelite images from DEFRA EO data service.

# eods-api-generate-cloudless-mosaic.ipynb
First run this Notebook which dowloads a list of all the Sentinel 2 images that are in the Area of interest difined within the Notebook. This is saved as two separate 
cvs that are needed in the EODS_API Notebook.

# EODS_API.ipynb
This Notebook dowloads the lsit og Sentinel 2 sattelite images using the two csv created in the previous Notebook. Additionally this Notebook will also create a mosaic of the downloaded images, mask them using a shapefiles and finally calculate the NDVI of the clipped image. 

For this notbook to work correctly the RSGISLIB (https://www.rsgislib.org/) for Jupiyter Notebook is needed. 
To make a conda install of this foloow the instructions below. 

1. Create the conda environment and install the two libraries  needed (rsgislib and jupyter) with:

$ conda create --name rsgislibenv -c conda-forge rsgislib jupyter
 
2. activate the environment you just created with:

$ conda activate rsgislibenv
 
3. start the jupyter notebook server which should launch in a browser or give the localhost URL:

$ jupyter notebook
 
