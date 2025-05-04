![Welcome Aboard](https://www.icegif.com/wp-content/uploads/titanic-icegif-16.gif)

# Welcome Aboard the Titanic 🚢 !!!!

This project explores various machine learning models to predict passenger survival on the Titanic. Using feature engineering, model evaluation, and hyperparameter tuning, we identify the most effective model for accurate predictions.

# Tools and Libaries used 🌹
- Python
- Pandas
- Numpy
- Sklearn
- Matplotlib
- seaborn 

### Hypothesis 

  - ## **While Looking through this data, My early Hypothesis is that, females, are customers that have/had higher fares are/were more likely to survive!**

# 🔍 Project Steps Explained 

## This project uses the Titanic dataset to train and evaluate machine learning models. Here's what happens step by step:

1. Data Cleaning & Feature Engineering
 - We handle missing values, convert text data into numbers (like Sex and Embarked), and scale numeric columns to make the data model-ready.

2. Model Selection & Training
 - Multiple machine learning models are trained, including:
     - Logistic Regression
     - Random Forest
     - Gradient Boosting
     - Naive Bayes
Each model is tested to see how well it predicts who survived.

3. Model Evaluation
- We compare model performance using:
    - Accuracy – how many predictions were correct
    - F1 Score – balance of precision and recall
    - ROC-AUC – how well the model separates survivors from non-survivors
4. Threshold Optimization

- Instead of using the default 0.5 cutoff, we find the best threshold that gives the highest F1 Score or AUC for more reliable predictions.
5. Hyperparameter Tuning
- For the best model (Gradient Boosting), we use Grid Search to find the ideal settings like:
    - Number of trees (n_estimators)
    - Learning rate
    - Tree depth
      - And more...
6. Final Prediction

After selecting and tuning the best model, we use it to make predictions on the test data.

# To see my results, all aboard and enjoy the voyage!!!