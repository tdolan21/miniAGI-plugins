# ML and Data Visualization App with Streamlit

## Overview
This is a Streamlit application for data visualization and machine learning model training. Users can upload a CSV file, visualize the data, select a machine learning model, and evaluate its performance. Advanced model visualization using SHAP is also provided.

## Install
To install this plugin drag the python file into the miniAGI pages directory. The docker environment will have the neccesary requirements.

## Key Components

### Imports
- Various machine learning and data visualization libraries like `sklearn`, `plotly`, `pandas`, `numpy`, and `shap`.

### Features

#### Data Upload and Preview
- Users can upload a CSV file.
- The app provides a preview of the data and handles missing values.

#### Data Visualization
- Users can select chart types (`Scatter`, `Box`, `Histogram`) and the axes for visualization.

#### Model Selection and Training
- Users choose the target and input variables.
- One-hot encoding is applied for categorical variables.
- Model choices: `Linear Regression`, `Random Forest`, `SVM`.
- Hyperparameter tuning with sliders.

#### Model Evaluation
- Metrics like MSE, MAE, and R-squared are displayed.

#### Advanced Model Visualization with SHAP
- SHAP values for `Random Forest` and `Linear Regression`.
- Displays SHAP force plot and summary plot for deeper insights.

## Usage
1. Run miniAGI and click the new page.
2. Upload a CSV file.
3. Visualize the data using the chart options.
4. Select target and input variables.
5. Choose the model type and tune hyperparameters.
6. Evaluate the model.
7. View advanced SHAP visualizations for model explanations.

## Note
- CSV files with missing values will have the NaN values automatically removed

## Future Work
- Extend support for more machine learning algorithms.
- Add more advanced metrics for model evaluation.


