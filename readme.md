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

1. Exploratory Data Analysis (EDA)

The EDA phase provided insights into the Titanic dataset's structure, feature relationships, and survival patterns. Here's a summary of the key findings and methods used:

📌 Data Overview & Cleaning
 **Missing Values:**
- Age was imputed using the median age grouped by Pclass and Sex.
- Cabin was dropped after engineering a new binary feature, HasCabin, indicating the presence or absence of a cabin record.
**Feature Engineering:**
- Created AgeGroup by binning ages into meaningful ranges.
- Converted Sex and Embarked to numeric formats for modeling.

**📊 Univariate Analysis**
- Survival Rate: About 37% survived.
- Sex: Roughly twice as many males as females were on board.
- Embarked: Most passengers boarded at Southampton.
- Class Distribution: Majority were lower class; upper class had the fewest.
- Cabins: Most passengers did not have cabin information.

**📊 Bivariate Insights**
- AgeGroup vs Sex: Most passengers were in the 21–30 age group, with decreasing counts as age increased.
- Survival vs AgeGroup: 21–30 was the most populated group among both survivors and non-survivors.
- Survival vs Pclass: lower class passengers had the highest death rate; upper class had the highest survival.
- Fare Distribution: Right-skewed with a few very high values, often associated with upper class.
- Family Features (SibSp, Parch): Most traveled alone or with 1–2 relatives.

**📈 Multivariate Analysis**
- Age vs Multiple Features: Trends showed older passengers were more likely to be in upper classes and have cabins.
- Scatter (Age vs Fare): Survivors often paid higher fares and were in upper classes.
- Boxplot (Fare vs Sex vs Survival): Females generally paid higher fares and had better survival rates.

**🔥 Correlation & Pairplot**

*Correlations:*
- Strong negative correlation between Pclass and Survived.
- Positive correlation between Fare, Sex (female=1), HasCabin, and Survived.

*Pairplot Findings:*
High fares and being female were strong indicators of survival.
Larger families (SibSp, Parch) were weakly associated with lower survival rates.


2. Data Cleaning & Feature Engineering
 - We handle missing values, convert text data into numbers (like Sex and Embarked), and scale numeric columns to make the data model-ready.

3. Model Selection & Training
 - Multiple machine learning models are trained, including:
     - Logistic Regression
     - Random Forest
     - Gradient Boosting
     - Naive Bayes
Each model is tested to see how well it predicts who survived.

4. Model Evaluation
- We compare model performance using:
    - Accuracy – how many predictions were correct
    - F1 Score – balance of precision and recall
    - ROC-AUC – how well the model separates survivors from non-survivors

5. Threshold Optimization
- Instead of using the default 0.5 cutoff, we find the best threshold that gives the highest F1 Score or AUC for more reliable predictions.

6. Hyperparameter Tuning
- For the best model (Gradient Boosting), we use Grid Search to find the ideal settings like:
    - Number of trees (n_estimators)
    - Learning rate
    - Tree depth
      - And more...

7. Final Prediction using test data 

After selecting and tuning the best model, we use it to make predictions on the test data.

# To see my results, all aboard and enjoy the voyage!!!
(https://mediaproxy.snopes.com/width/1200/https://media.snopes.com/2010/03/GettyImages-590676055.jpg)