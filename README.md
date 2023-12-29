# Project-2
Trading system using two kinds of Autoencoder.
# Data Source
Kaggle
('https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists?select=aug_test.csv')

# Problem Definition
Make a prediction about whether you'll change jobs or not.

# Target Type
Binary Classification

# EDA Explanation
-The target data is unbalanced. To solve the problem I used a SMOTE

-RandomizedSearchCV

# Model(Using Hyperparameter)
| Name | Accuracy | Auc_curve  | Best_score |
| :------: | :------: | :------: | :------: |
| DT | 0.75 | 0.79 | 0.78 |
| RF | 0.77 | 0.78 | 0.75 |
| GB | 0.79 | 0.79 | 0.82|
| XGB | 0.78 | 0.8 | 0.83 |
| LGB | 0.78 | 0.79 | 0.82 |
| Stacking(LGB) | 0.78 | 0.79 | 0.8 |

