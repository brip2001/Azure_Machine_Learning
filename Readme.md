# Udacity Machine Learning Project - Optimizing a Pipeline in Azure

## Project Overview
This project focuses on optimizing a machine learning pipeline using **Azure Machine Learning**. The primary goal is to implement hyperparameter tuning for a Logistic Regression model and explore the capabilities of **AutoML** for comparison.

## Dataset
The dataset used in this project is the **Bank Marketing Dataset**, available publicly. It contains information about customer interactions and whether or not they subscribed to a term deposit.

- **Source**: UCI Machine Learning Repository
- **Size**: 41,188 records
- **Features**: 21 attributes (such as age, job, marital status, education, etc.)

## Architecture and Methodology
The solution consists of the following key steps:

1. **Data Preprocessing**: The dataset is cleaned, and categorical columns are one-hot encoded for use in a machine learning model.
   
2. **Training Logistic Regression Model**: Hyperparameters like regularization strength (`C`) and maximum iterations (`max_iter`) were tuned using Azure's HyperDrive service.
   
3. **AutoML for Comparison**: Azure's AutoML service was used to compare multiple models and automatically select the best one based on accuracy.

## Files in the Project
- **train.py**: The training script for the Logistic Regression model.
- **udacity-project.ipynb**: Jupyter notebook with HyperDrive and AutoML runs.
- **README.md**: Documentation.

## Results
- The best-performing Logistic Regression model had an accuracy of X%.
- AutoML selected the Y algorithm, which achieved an accuracy of Z%.

## Setup Instructions
1. Clone the repository to your local machine.
2. Run `train.py` on Azure Machine Learning Studio or a local environment with access to the dataset.
3. Configure a compute cluster using Standard_D2_V2 for training.

## Conclusion
Azure Machine Learning provides a scalable and easy-to-use platform for deploying machine learning pipelines, offering tools like HyperDrive and AutoML for efficient experimentation and model optimization.
