# Kaggle_infectious-disease-prediction
Kaggle Data Set about Infectious diseases in USA 2001-2014
https://www.kaggle.com/datasets/haithemhermessi/infectious-disease-prediction

## Overview

This repository contains the analysis and predictive modeling of infectious disease cases in California. The data spans from 2001 to 2014 and includes various diseases, demographic information, and statistical measures. The goal is to use data science and machine learning techniques to predict the occurrence and spread of these diseases, helping to advance medical research and public health initiatives.

## Dataset

The dataset includes records of disease cases reported to the California Department of Public Health (CDPH). The data is structured with the following columns:

- **Disease**: The name of the disease reported for the patient.
- **County**: The county in which the case resided when they were diagnosed and/or where they are currently receiving care.
- **Year**: The year derived from the estimated illness onset date.
- **Sex**: The sex of the patient (Male, Female).
- **Count**: The number of occurrences of each disease that meet the surveillance definition and/or inclusion criteria.
- **Population**: The estimated population size for each County, Year, Sex strata.
- **Rate**: The rate of disease per 100,000 population.
- **CI.lower**: The lower bound of the 95% confidence interval for the calculated rate.
- **CI.upper**: The upper bound of the 95% confidence interval for the calculated rate.
- **Disease_Category**: Categorical information about the disease.
- **Symptom_Category**: Categorical information about the symptoms associated with the disease.

## Context

The data was extracted from California Confidential Morbidity Reports and/or Laboratory Reports submitted to CDPH by September 2015. These reports included cases that met the surveillance case definition for various diseases. The data has been cleaned and split into training and test datasets, with the training dataset containing 75,614 rows and the test dataset containing 18,904 rows.

## Features

### Disease
- **Description**: The name of the disease reported for the patient.

### County
- **Description**: The county in which the case resided when they were diagnosed and/or where they are currently receiving care.

### Year
- **Description**: The year is derived from the estimated illness onset date.
- **Values**: Years spanning 2001-2014.

### Sex
- **Description**: The sex of the patient.
- **Values**: Male, Female.

### Count
- **Description**: The number of occurrences of each disease that meet the surveillance definition and/or inclusion criteria for that County, Year, Sex strata.
- **Source**: [CDC National Surveillance Case Definitions](http://wwwn.cdc.gov/nndss/case-definitions.html)

### Population
- **Description**: The estimated population size for each County, Year, Sex strata.
- **Source**: [California Department of Finance Population Projection Data](http://www.dof.ca.gov/research/demographic/reports/view.php)
- **Values**: Positive integers.

### Rate
- **Description**: The rate of disease per 100,000 population for the corresponding County, Year, Sex strata.
- **Calculation**: `Rate = (Count * 100,000) / Population`
- **Values**: Positive real numbers.

### CI.lower
- **Description**: The lower bound of the 95% confidence interval for the calculated rate.
- **Calculation Method**: Exact Pearson-Klopper method using the R `binom` package.
- **Values**: Positive real numbers.

### CI.upper
- **Description**: The upper bound of the 95% confidence interval for the calculated rate.
- **Calculation Method**: Exact Pearson-Klopper method using the R `binom` package.
- **Values**: Positive real numbers.

## Goals

1. **Exploratory Data Analysis (EDA)**: Understand the distribution and trends of diseases across different counties, years, and demographics.
2. **Predictive Modeling**: Develop machine learning models to predict disease occurrence and rates based on the available data.
3. **Visualization**: Create visualizations to effectively communicate the findings and predictions.

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Jupyter Notebook or JupyterLab
- Required Python packages (see `requirements.txt`)

### Installation
**Clone the repository**: git clone https://github.com/yourusername/infectious-disease-prediction.git
