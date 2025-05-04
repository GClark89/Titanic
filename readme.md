![Welcome Aboard](https://www.icegif.com/wp-content/uploads/titanic-icegif-16.gif)

# Welcome Aboard the Titanic 🚢 !!!!
🚢 Titanic Dataset Overview

🧩 The Challenge
The sinking of the Titanic is one of the most infamous shipwrecks in history.
On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1,502 out of 2,224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, we ask you to build a predictive model that answers the question:
“What sorts of people were more likely to survive?”
using passenger data (i.e., name, age, gender, socio-economic class, etc.).

|📊 Data Dictionary|
|Variable| Description|
|---------|-------------|
|Survival |	0 = No, 1 = Yes|
|Pclass	   |Ticket class; 1 = 1st, 2 = 2nd, 3 = 3rd|
|Sex	    |Male or Female|
|Age	|Age in years|
|SibSp	|# of siblings/spouses aboard the Titanic
|Parch	|# of parents/children aboard the Titanic
|Ticket	|Ticket number
|Fare	|Passenger fare
|Cabin	|Cabin number
|HasCabin	|Created column: 0 = no cabin, 1 = has cabin
|Embarked	|Port of Embarkation: C = Cherbourg, Q = Queenstown, S = Southampton


## 📝 Variable Notes
Pclass – A proxy for socio-economic status (SES):

- 1st = Upper
- 2nd = Middle
- 3rd = Lower
- Age – Fractional if less than 1; if estimated, represented as xx.5.

SibSp – Sibling = brother, sister, stepbrother, stepsister
Spouse = husband, wife (mistresses and fiancés were ignored)

Parch – Parent = mother, father
Child = daughter, son, stepdaughter, stepson
Some children travelled only with a nanny, therefore Parch = 0 for them.



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

## This project uses the Titanic dataset to train and evaluate machine learning models. Here's a breakdown:

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