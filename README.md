# Load Type Classifier

## Overview
This project aims to build a machine learning model to predict the "Load_Type" of a power system based on historical data. The classification categories are:
- Light_Load
- Medium_Load
- Maximum_Load

The model leverages time series features and power system measurements to accurately classify the load type.

## Dataset Description
The dataset contains the following columns:
- **Date**: Continuous-time data taken on the first of the month
- **Usage_kWh**: Industry energy consumption (continuous, kWh)
- **Lagging Current reactive power**: Continuous (kVarh)
- **Leading Current reactive power**: Continuous (kVarh)
- **CO2**: Continuous (ppm)
- **NSM**: Number of Seconds from Midnight (continuous, S)
- **Load Type**: Categorical (Light_Load, Medium_Load, Maximum_Load)

## Approach
1. **Data Loading**: Import the dataset and inspect its structure.
2. **Data Preprocessing**: Rename columns and handle missing values using appropriate imputation methods.
3. **Feature Engineering**: Create new features (e.g., hour, log transforms, power factor types) and resample data to hourly intervals and  Convert the target variable (Load_Type) into numerical labels for classification.
4. **Feature Selection**: Drop irrelevant columns and select the most informative features for modeling.
5. **Exploratory Data Analysis (EDA)**: Visualize feature distributions, correlations, and temporal patterns.
6. **Validation Strategy**: Use the last month of data as the test set to simulate real-world forecasting.
7. **Modeling**: Train a Random Forest classifier (or other models) on the training set.
8. **Evaluation**: Assess model performance using accuracy, precision, recall, F1-score, and confusion matrix.
9. **Reporting**: Analyze feature importances and summarize findings.

## Usage
1. Clone this repository and navigate to the project directory.
2. Ensure the dataset is in the `data/` folder as `load_data.csv`.
3. Open and run the `load_type_classifier.ipynb` notebook step by step.



Install requirements with: pip instal -r requirements.txt

## Possible Improvements
- Try Deep learning models (RNNs, LSTM)
- Hyperparameter tuning

