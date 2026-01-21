README

This repository contains all files used for dataset preparation, model training, evaluation, and report generation for the project "Predicting the Most Probable Species Occurrence from Environmental and Spatial Variables".

Folder Structure

50/
|
| — report /                                    # LaTeX report and related assets
| — dataset /                                  # Final processed Train/Test datasets
| — dataprep /                               # Scripts and files used to build the final dataset
|
| — Dataset_Preparation.ipynb     # Notebook for generating the dataset (optional)
| — MainModelTraining.ipynb       # Notebook for preprocessing, training & evaluation
|
| — requirements.txt                      # For model training only
| — requirements_dataprep.txt      # Extra dependencies for dataset regeneration
|
| — README.txt



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

Ensure your current working directory (pwd) is the main folder (50/) so that all relative paths work correctly.

Example:
cd /path_to_50/

How to Run

A. Dataset Preparation (Optional)

The final dataset is already prepared and stored in the dataset/ folder. If you wish to regenerate it:

* Download the Copernicus Land Cover dataset from the link: https://cds.climate.copernicus.eu/datasets/satellite-land-cover?tab=download&slug=satellite-land-cover
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

Report

All LaTeX report files are available under the report/ folder. Compile using any standard LaTeX environment if needed.

Notes

Paths inside the notebooks are relative and assume the root directory is 50/.
No additional dataset downloads or external dependencies are required.