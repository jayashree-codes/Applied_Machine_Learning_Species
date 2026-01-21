README

This repository contains all files used for dataset preparation, model training, evaluation, and report generation for the project "Predicting the Most Probable Species Occurrence from Environmental and Spatial Variables".

Setup Instructions

1. Dependencies
This project uses two separate requirements files:

(i) requirements.txt (Default)
Contains only the libraries required for running:
MainModelTraining.ipynb - Basic Preprocessing, Model training, Evaluation and performance analysis
Install with:
pip install -r requirements.txt


(ii) requirements_dataprep.txt (Optional – only if regenerating the dataset)
Use this only if you want to re-run Dataset_Preparation.ipynb. It includes additional geospatial and environmental libraries, which may require system dependencies on some OS.

Install with:
pip install -r requirements_dataprep.txt

If you do not need to regenerate the dataset, you can ignore this file.

2. Working Directory

Ensure your current working directory (pwd) is the main folder (project/) so that all relative paths work correctly.

Example:
cd /project/

How to Run

A. Dataset Preparation (Optional)


To generate dataset:

* Download the Copernicus Land Cover dataset from the link: https://cds.climate.copernicus.eu/datasets/satellite-land-cover?tab=download&slug=satellite-land-cover
 This file is large in size. After downloading, place it inside the dataprep/ folder before running Dataset_Preparation.ipynb.
* Download the Climate Data from the link: https://www.worldclim.org/data/monthlywth.html
  This file is large in size. After downloading, place it inside the dataprep/ folder before running Dataset_Preparation.ipynb.
* Download the Global Administrative Areas Data from the link: https://gadm.org/download_country.html
  This file is large in size. After downloading, place it inside the dataprep/ folder before running Dataset_Preparation.ipynb.
* Download the Global Ocean and seas Data from the link: https://www.marineregions.org/download_file.php?name=GOaS_v1_20211214.zip
  This file is large in size. After downloading, place it inside the dataprep/ folder before running Dataset_Preparation.ipynb.
* Open Dataset_Preparation.ipynb
* Run the notebook cells
* It uses files inside the dataprep/ folder to recreate the processed dataset.

B. Model Training & Evaluation

To train and evaluate the models:

* Open MainModelTraining.ipynb
* Run all cells sequentially
* The notebook performs:
   - Data loading
   - Preprocessing
   - Dimensionality reduction
   - Hyperparameter search
   - Model training
   - Evaluation with Test data
   - Error and Performance analysis

Notes

Paths inside the notebooks are relative and assume the root directory is path_to_project/.
No additional dataset downloads or external dependencies are required.
