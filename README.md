# neurofive-ml-track
# Neurofive ML Track

This repo documents my Machine Learning internship tasks at Neurofive Solutions, using the Titanic dataset ("Titanic - Machine Learning from Disaster" from Kaggle).

## Task 1: Exploratory Data Analysis (EDA)
- Loaded the dataset and inspected it with `.info()`, `.describe()`, `.head()`
- Identified 891 rows, 12 columns
- Found missing values in `Age` (177), `Cabin` (687), and `Embarked` (2)

## Task 2: Data Cleaning & Visualization
- Filled missing `Age` with median, `Embarked` with mode, dropped `Cabin` (77% missing)
- Detected outliers in `Fare` using a boxplot
- Built 4 visualizations: histogram, boxplot, bar chart, correlation heatmap
- Found `Pclass` had the strongest correlation with survival (-0.34)

## Task 3: Logistic Regression Model
**Approach:**
- One-hot encoded `Sex` and `Embarked` using `pd.get_dummies()`
- Selected features: `Pclass`, `Age`, `SibSp`, `Parch`, `Fare`, `Sex_male`, `Embarked_Q`, `Embarked_S`
- Split data 80/20 into training and test sets using `train_test_split`
- Trained a Logistic Regression model with `scikit-learn`

**Results:**
- **Accuracy: ~81%**
- Confusion Matrix: 90 true negatives, 55 true positives, 15 false positives, 19 false negatives
- The model performs slightly better at identifying passengers who did not survive than those who did

## Files
- `neurofive.solution task .ipynb` — full notebook with EDA, cleaning, visualizations, and model
- `train.csv` — dataset used
