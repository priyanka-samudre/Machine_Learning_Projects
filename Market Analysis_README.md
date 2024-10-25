# Project Overview: Market Analysis
This project aims to predict the success of a bank marketing campaign based on customer data using a Decision Tree classifier. The dataset consists of information about individuals contacted for the campaign, such as their job, marital status, education, and financial attributes. The target variable is whether the client subscribed to the bank’s product (y), which is a binary outcome.

## Steps Followed:
#### Data Wrangling:

The dataset was cleaned and transformed for modeling. Key transformations included converting categorical variables to numeric formats using Ordinal Encoding and categorizing the balance column into different classes.
Removed irrelevant features such as day, poutcome, and pdays that were not contributing significantly to the model's performance.
Added new binary columns like previous_bool and transformed boolean columns like default, housing, and loan.
#### Feature Engineering:

Categorical features like job, marital status, and education were encoded using an ordinal encoder to make them suitable for the Decision Tree model.
The balance feature was classified into different classes for more effective feature utilization.
#### Modeling:

A Decision Tree Classifier was used to predict the outcome of the marketing campaign.
Hyperparameter tuning was performed using GridSearchCV to optimize model performance. The parameters tuned include max_depth, criterion, min_samples_split, and min_samples_leaf.
#### Model Evaluation:

The model was evaluated using precision, recall, F1-score, and accuracy metrics.
A confusion matrix was generated to understand the model’s performance across True and False classes.
## Key Learnings:
Feature Selection: Some features had little impact on the model’s prediction, and removing them improved the model's performance.

Data Imbalance: The dataset had a significant class imbalance, where the majority of clients did not subscribe to the product. This led to high precision for the False class but poor performance for the True class. Addressing this imbalance (e.g., through resampling techniques) could improve the model's predictive power for the minority class.

Hyperparameter Tuning: Tuning the depth of the decision tree and adjusting other parameters helped in preventing overfitting and improving model generalization.
## Conclusion:
The Decision Tree classifier provided a good accuracy of 88%, especially for the majority class (False). However, due to the class imbalance, the model struggled with identifying True cases (campaign success). To enhance the model further, future iterations could focus on addressing the class imbalance and experimenting with different models such as Random Forest or boosting algorithms.
