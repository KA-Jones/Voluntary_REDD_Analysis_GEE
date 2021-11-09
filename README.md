# Voluntary REDD Analysis (Google Earth Engine)

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Create Annual Forest Asset](#create-annual-forest-asset)
* [Generate Forest Time Series](#generate-forest-time-series)

## General info
Generate annual time series measuring forest coverage in for all municipalities in the Brazilian Amazon. Annual land use/cover classifications from [MapBiomas](https://mapbiomas.org/) provide data between 1985 and 2019 using the Collection 5 dataset.

Based on [Voluntary REDD Analysis](https://github.com/thaleswest/Voluntary-REDD-analysis) developed by Thales West.

	
## Technologies
Project is created with:
* Google Earth Engine Python API
* Google Colab

	
## Setup
To run this project, access the workfow using a Google Colab Notebook:
- [Google Earth Engine](https://earthengine.google.com/) account

Or, to access using Jupyter in Windows:
- Follow the [Python Installation](https://developers.google.com/earth-engine/python_install) Guide


---



The workflow to generate time series is broken into two parts: 

1.   Create Annual Forest Asset - Correct Prohibited Land Use/Cover Transitions
2.   Generate Forest Time Series

---


## Create Annual Forest Asset


**Input:** MapBiomas Collection 5

**Output:** One image corrected for probited land cover transitions.
The output image is saved as an Earth Engine asset which is analyzed in Part 2: Generate Forest Time Series. Once Part 1 is complete, the image asset may be used indefinitely. If a new MapBiomas Collection is released and/or the years included in the proposed study period change, Part 1 will need to be executed again to create a new asset that matches the project requirements.

**Please note**, due to how data are filtered and modified, changing the years of the study will influence the amaount of forest that is measured. Annual land cover is modified using temporal filters that "look" back and forward in time. Thus, changing the study years impacts what land cover data is available to process and generate annual forest cover time series.

---


## Generate Forest Time Series

**Input:** Image Asset (Step 1) saved to Earth Engine Assets

**Output:** One image corrected for probited land cover transitions

**REQUIRED:**

You must complete [PART 1: Data Processing](https://github.com/KA-Jones/Voluntary_REDD_Analysis_GEE/blob/master/Create_Annual_Forest_Asset.ipynb) before generating forest coverage time series.

-OR-

Have access to a previous Image Asset created as the result of using PART 1: Data Processing.
