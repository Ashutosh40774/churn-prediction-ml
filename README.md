
Customer Churn Prediction using Machine Learning

Project Overview
This project aims to predict customer churn using various machine learning models with SMOTE to handle class imbalance. It includes model comparison, performance analysis, and a clear deployment-ready structure.

Project Structure
data/: Dataset file (`telco_churn.csv`) and cleaned csv is also available.
All the data is taken from Kaggle  
notebooks/: Jupyter notebooks for each modeling phase
plots/: Visual outputs like model comparison charts
scripts/: Utility scripts for preprocessing, evaluation, and VIF checks

Models Compared

| Model                  | Accuracy | Recall | Precision | F1-score | ROC AUC |
|------------------------|----------|--------|-----------|----------|---------|
| Logistic + SMOTE       | 0.815    | 0.829  | 0.81      | 0.82     | 0.902   |
| XGBoost + SMOTE        | 0.823    | 0.843  | 0.81      | 0.83     | 0.908   |
| **Stacked + SMOTE**    | 0.828    | 0.840  | 0.82      |0.83      | 0.915   |
| NN + SMOTE (Original)  | 0.804    | 0.871  | 0.77      | 0.82     | 0.903   |
| NN + SMOTE (Improved)  | 0.82     | 0.85   | 0.81      | 0.83     | 0.904   |

Best Model

Stacked + SMOTE achieved the best average score across all metrics.

Visualizations
Model comparison chart:

Requirements
- Python >= 3.8
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn
- xgboost

Usage
Run notebooks in order:
1. 01_data_cleaning_eda.ipynb`
2. 02_logistic_smote.ipynb`
3. 03_xgboost_smote.ipynb`
4. 04_stacked_smote.ipynb`
5. 05_nn_smote.ipynb`
6. 06_model_comparison.ipynb`

NOTE : IF you are using the final_churn_dataset.csv then directly import into models and run.