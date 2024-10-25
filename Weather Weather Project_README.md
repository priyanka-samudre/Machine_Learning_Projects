# Seattle Weather Analysis Project Using XGBoost
## Project Overview
The project aims to build a predictive model for classifying weather conditions in Seattle using historical weather data. The model leverages the XGBoost classifier, a powerful machine learning algorithm, to achieve high accuracy in multi-class weather predictions based on various weather features like precipitation, temperature, and wind speed.

## Steps and Methodology
#### 1. Data Loading and Preparation
Data Loading: The dataset (seattle-weather.csv) is loaded into a Pandas DataFrame.

Missing Value Check: Verified that the dataset has no missing values.

Label Encoding: The weather column is encoded into numerical labels using Label Encoding to make it suitable for the model.
#### 2. Data Normalization
Feature Scaling: All numeric features (precipitation, temp_max, temp_min, wind) are normalized to bring them into the same range, ensuring that all features have equal importance during model training.
#### 3. Data Splitting
Train-Test Split: The data is split into training (80%) and testing (20%) sets for model evaluation.
#### 4. Model Training
XGBoost Classifier: An XGBoost classifier is trained using the training dataset to learn the patterns associated with different weather conditions.

Hyperparameter Tuning: GridSearchCV is used to perform hyperparameter tuning for gamma and learning_rate to optimize the model's performance.
#### 5. Model Evaluation
Accuracy Score: The accuracy of the model on the test set is 80.8%, indicating a good performance.

Classification Report: Generated a classification report to understand precision, recall, and F1-scores for each weather class, identifying areas for improvement in classes with lower precision and recall values.
#### 6. Model Optimization
Best Model Selection: The GridSearchCV identified the best parameters (gamma=1, learning_rate=0.1), improving the overall model performance.
## Key Learnings
#### 1. Data Preparation
Handling and encoding categorical data (weather conditions) is critical for model compatibility and effectiveness.
#### 2. Normalization
Feature scaling ensures that all input features contribute equally to the model's learning process.
#### 3. Hyperparameter Tuning
GridSearchCV enables finding the optimal parameters for the XGBoost model, significantly enhancing its accuracy and performance.
#### 4. Model Evaluation
The use of accuracy scores and classification reports allows for a deeper understanding of model performance and highlights areas that may require further tuning or data preprocessing.
#### 5. Working with XGBoost
XGBoost’s flexibility and efficiency make it a powerful choice for classification tasks, especially when dealing with multi-class problems.
## Tools and Libraries Used
Pandas and NumPy: For data manipulation and preprocessing.

Scikit-learn: For splitting the dataset, evaluation metrics, and hyperparameter tuning (GridSearchCV).

XGBoost: For building and training the classification model.

Matplotlib and Seaborn: For data visualization and exploratory analysis.
