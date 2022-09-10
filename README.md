# Predicting Building Site Energy Usage

Semester project for UC Berkeley MIDS Intro to Machine Learning - Summer 2022  

Project team: CJ Donahoe, Ben Meier, Sam Rosenberg; code contained within project is my own

Technical skills: Keras TensorFlow, Linear Regression, Random Forest, Data preprocessing, Hyperparameter tuning, Jupyter Notebooks, Google Colab, Git, EDA, Data Visualization, Python, Pandas, Matplotlib, Seaborn

## Introduction

Can we predict site energy usage from publically available building performance data? This project aims to predice building site energy usage as measured by energy use intentisty (kBtu/square feet). Notebooks written via Google Colab environment.

## Data Source

Data was downloaded from the building performance database (https://bpd.lbl.gov/). Data was contained in 16 separate CSVs collected by various state and municipal governments in collaboration with the DOE. More info about project this project can be founda at https://www.energy.gov/eere/buildings/building-performance-database-bpd. Data downloaded on June 5, 2022 (BPD_csvs.zip). 

## Data Cleansing

EDA notebook to perform data clean-up and consolidation, create one-hot and mulihot features. Output data pickled for using in additional notebooks.

## Models

Several models were developed to predict site energy usage (see project presentation).
- Linear regression
    - The final model developed was a normalized linear model with multihot encoding for facility use, roof type, heating and cooling system, window glass type, wall construction, and climate.
- Random forest
    - Final model has a maximum depth of 16, minimum number of samples per leaf of 5, and a forest with 500 trees. Includes same multihot encoding as linear regression.

## Project Presentation

See PDF for the final project presentation. Final results indicate random forest model is most successful in predicting site energy usage. This is likely due to inconsitent dataset features and standardation between municipalities. Additional data collection should focus on standardizing feature collection across regions.