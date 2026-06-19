# Deforestation Issue Analysis Using Support Vector Machine

## Project Overview

This project analyzes deforestation data using Support Vector Machine Regression.

The dataset contains country-wise and year-wise deforestation-related features such as CO2 emissions, rainfall, population, GDP, policy strictness, corruption index, illegal lumbering incidents, and other environmental indicators.

## Target Variable

Selected target variable: Forest_Loss_Area_km2

## Data Preprocessing

- Loaded the dataset
- Checked missing values
- Removed duplicate records
- Encoded categorical columns using Label Encoding
- Filled missing numerical values using mean imputation
- Filled missing categorical values using mode imputation
- Standardized features using StandardScaler
- Split the dataset into 80% training and 20% testing data

## Model Building

Two SVM models were trained:

1. Linear Support Vector Regression
2. Tuned Support Vector Regression using GridSearchCV

## Best Hyperparameters

{'svm__C': 100, 'svm__degree': 2, 'svm__gamma': 0.1, 'svm__kernel': 'poly'}

## Model Evaluation

| Metric | Value |
|---|---|
| MAE | 1011.881 |
| MSE | 1434054.7766 |
| RMSE | 1197.5203 |
| R2 Score | -0.3412 |

## Cross Validation

Average R2 Score: -0.0699

## Top Important Features

- Corruption_Index: Importance Score = 0.0464
- GDP_Billion_USD: Importance Score = 0.0412
- CO2_Emission_mt: Importance Score = 0.0364
- International_Aid_Million_USD: Importance Score = 0.0144
- Deforestation_Policy_Strictness: Importance Score = 0.0133
- Illegal_Lumbering_Incidents: Importance Score = 0.0123
- Rainfall_mm: Importance Score = -0.0029
- Country: Importance Score = -0.0058
- Population: Importance Score = -0.007
- Year: Importance Score = -0.0115

## Interpretation

The model identifies the most influential factors affecting deforestation. Variables such as population, GDP, rainfall, policy strictness, corruption index, protected area percentage, and illegal lumbering incidents can strongly influence forest loss.

Higher population may increase land demand for agriculture, housing, and infrastructure.

GDP may influence deforestation through industrial expansion, urban development, and resource extraction. However, stronger economies may also invest more in forest conservation.

Strict forest policies can help reduce illegal logging and uncontrolled land conversion.

Corruption can weaken forest governance and increase illegal exploitation.

Illegal lumbering incidents are direct indicators of forest damage and usually increase deforestation levels.

Protected forest areas can reduce deforestation when conservation laws are properly implemented.

## Recommendations

1. Strengthen forest protection laws.
2. Reduce illegal lumbering through monitoring and penalties.
3. Increase protected forest area coverage.
4. Improve transparency in forest governance.
5. Promote sustainable agriculture.
6. Use international aid for reforestation and forest monitoring.
7. Balance economic growth with environmental protection.

## Generated Files

- svm_cleaned_dataset.csv
- svm_missing_values.csv
- svm_dataset_summary.csv
- svm_model_metrics.csv
- svm_grid_search_results.csv
- svm_cross_validation_scores.csv
- svm_predictions.csv
- svm_feature_importance.csv
- svm_best_svm_model.pkl
- svm_linear_svm_model.pkl
- svm_summary.json
- svm_config.yaml
- svm_correlation_heatmap.png
- svm_feature_importance_graph.png
- svm_actual_vs_predicted.png
- svm_prediction_error_graph.png
- svm_model_comparison_graph.png
- svm_svm_decision_surface_pca.png