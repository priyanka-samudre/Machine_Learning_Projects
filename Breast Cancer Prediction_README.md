# Breast Cancer Prediction Using Decision Tree Classifier
## Project Overview
The objective of this project is to build a model that classifies whether a tumor is malignant or benign based on the dataset’s features. The dataset contains various characteristics of tumors such as radius, texture, perimeter, area, and smoothness. The model uses a Decision Tree Classifier to predict the diagnosis and evaluate its accuracy.

## Steps and Methodology
#### 1. Data Loading and Exploration
The dataset is loaded using Pandas, and it is checked for missing values, which were confirmed to be zero, indicating a clean dataset.

A bar plot visualizes the distribution of diagnoses (M for malignant and B for benign), showing the count of each diagnosis.
#### 2. Data Preparation
The diagnosis column is encoded into binary values (1 for malignant and 0 for benign) to facilitate modeling.

The id column, which is irrelevant for prediction, is removed.
#### 3. Modeling with Decision Tree Classifier
The data is split into training (80%) and testing (20%) sets using train_test_split.

A basic Decision Tree Classifier is trained on the training set, achieving an accuracy of 92.98% on the test set.
#### 4. Hyperparameter Tuning
The depth of the Decision Tree is varied from 1 to 20 to find the optimal depth that balances training accuracy and cross-validation accuracy.

The cross-validation score, using 10-fold cross-validation, helps determine the model’s performance at each depth level.

Training accuracy reaches 100% as the depth increases, indicating overfitting. Cross-validation scores suggest that the best performance is achieved at depths between 5 and 10, with scores around 92%.
## Key Findings

Initial Model Performance: The Decision Tree model achieved 92.98% accuracy on the test set, showing strong predictive power.

Effect of Tree Depth: As the tree depth increases, training accuracy reaches 100%, showing overfitting. The cross-validation scores highlight the optimal depth range between 5 and 10.

## Conclusion
The Decision Tree Classifier demonstrates high accuracy in predicting whether a tumor is malignant or benign. However, careful tuning of the tree depth is necessary to prevent overfitting and maintain generalization capability.

## Tools and Libraries Used

Pandas and NumPy: For data manipulation and analysis.

Seaborn and Matplotlib: For data visualization.

Scikit-learn: For building and evaluating the Decision Tree Classifier.
