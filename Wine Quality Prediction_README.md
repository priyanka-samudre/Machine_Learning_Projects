# Wine Quality Prediction Using Machine Learning
## Overview
This project focuses on predicting wine quality using machine learning algorithms such as Random Forest and Support Vector Machine (SVM). It explores various steps, from data preprocessing to model evaluation, to classify wines based on their chemical properties. The goal is to determine which machine learning model offers the best performance in predicting wine quality.

## Steps
#### Data Collection:

The dataset was sourced from the UCI Machine Learning Repository, featuring red and white wine samples with multiple chemical attributes.
#### Data Preprocessing:

Handling Missing Values: Checked for any missing values and ensured data integrity.

Feature Scaling: Standardized the dataset using StandardScaler to ensure all features are on the same scale.

Label Encoding: Converted the target variable (wine quality) into binary categories (e.g., "good" or "bad") to simplify prediction tasks.
#### Exploratory Data Analysis (EDA):

Visualized distributions of wine quality across different chemical features.
Generated correlation heatmaps to identify relationships between variables.
#### Modeling:

Random Forest Classifier: Implemented as an ensemble method to capture feature importance and interactions between variables.
Support Vector Machine (SVM): Applied to maximize classification margin, particularly focusing on complex decision boundaries.
#### Hyperparameter Tuning:

Used GridSearchCV to perform hyperparameter tuning for both models, optimizing accuracy and model performance.
#### Evaluation:

Evaluated the models using accuracy, precision, recall, F1-score, and confusion matrix to understand their predictive capabilities.
## Key Learnings
Feature Importance: Through Random Forest, it became evident that certain features like alcohol content and volatile acidity significantly influenced wine quality. Understanding these key variables helped improve model performance.

Data Preprocessing Impact: Proper scaling and encoding were crucial for SVM performance, as it relies heavily on feature scaling for accurate predictions. This reinforced the importance of data preprocessing in machine learning pipelines.

Model Comparison: Random Forest provided better overall accuracy due to its ability to handle feature interactions effectively, while SVM showed competitive performance on well-separated classes.

Model Tuning: GridSearchCV was highly effective in optimizing model parameters, significantly improving the performance of both models.

## Conclusion
This project demonstrated the effectiveness of machine learning models, particularly Random Forest, in predicting wine quality. The importance of thorough data preprocessing and hyperparameter tuning was highlighted throughout the process. Random Forest emerged as the more suitable model due to its flexibility and ability to capture complex interactions between features, while SVM showed strong performance when the dataset was well-preprocessed.
