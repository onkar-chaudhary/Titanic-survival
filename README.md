# Titanic Survival Prediction
This project predicts whether a passenger survived the Titanic wreck based on available passenger data. The dataset includes demographic, ticket, and ship-related information to train a model that outputs predictions on survival.

# Dataset Overview
The project uses two CSV files: train.csv and test.csv. The columns are:

- **survival:** Survival (0 = No, 1 = Yes) - present only in the train dataset
- **pclass:** Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **sex:** Sex of the passenger
- **age:** Age in years
- **sibsp:** Number of siblings/spouses aboard the Titanic
- **parch:** Number of parents/children aboard the Titanic
- **ticket:** Passenger's ticket number
- **fare:** Passenger fare
- **cabin:** Cabin number (many missing values)
- **embarked:** Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

# Project Workflow
## 1. Data Preprocessing:

- Handling missing values in columns like age, fare, and embarked.
- Feature engineering, including:
- Creating a Cabin_Deck feature from the cabin column.
- Adding a Cabin_Missing binary column to indicate missing cabin data.
- One-hot encoding categorical variables (sex, embarked).
- Dropping unnecessary columns like ticket and the original cabin.

## 2. Model Building and Evaluation:

- An XGBoost model was trained to predict survival using the processed data.
- The model was evaluated using appropriate metrics on the training data.

## 3. Submission:

- After predicting on the test.csv file, a final submission file was created.

# Files
- **1. titanic.ipynb:** Jupyter notebook containing the full code for data preprocessing, model building, and evaluation.
- **2. data**: This folder contains the dataset (csv files) used.
  - **i) train.csv:** The training dataset used to train the model.
  - **ii) test.csv:** The test dataset used to generate predictions.
- **3. submission.csv:** The final predictions on the test dataset in the required format for submission.
