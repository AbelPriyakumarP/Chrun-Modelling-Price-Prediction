# Chrun-Modelling-Price-Prediction

## Overview
This project focuses on predicting customer churn using machine learning. The dataset used is `Churn_Modelling.csv`, which contains customer details and churn status.

## Dataset Information
The dataset consists of the following columns:
- **RowNumber**: Index
- **CustomerId**: Unique customer ID
- **Surname**: Customer's last name
- **CreditScore**: Credit score of the customer
- **Geography**: Country of the customer
- **Gender**: Male or Female
- **Age**: Age of the customer
- **Tenure**: Number of years the customer has stayed with the bank
- **Balance**: Account balance
- **NumOfProducts**: Number of bank products used
- **HasCrCard**: Whether the customer has a credit card (1: Yes, 0: No)
- **IsActiveMember**: Whether the customer is an active member (1: Yes, 0: No)
- **EstimatedSalary**: Estimated salary of the customer
- **Exited**: Whether the customer churned (1: Yes, 0: No) *(Target Variable)*

## Step-by-Step Guide

### 1. Data Preprocessing
- Load the dataset using Pandas.
- Handle missing values (if any).
- Encode categorical variables (e.g., `Geography`, `Gender`) using One-Hot Encoding or Label Encoding.
- Feature scaling using StandardScaler or MinMaxScaler.

### 2. Exploratory Data Analysis (EDA)
- Analyze data distribution using histograms, box plots, and pair plots.
- Correlation analysis to identify important features.
- Visualize churn rate in relation to key features.

### 3. Model Building
- Split the dataset into training and testing sets (e.g., 80-20 split).
- Use machine learning models such as:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - Support Vector Machine (SVM)
  - XGBoost
- Train and tune models using hyperparameter optimization (e.g., GridSearchCV or RandomizedSearchCV).

### 4. Model Evaluation
- Use performance metrics:
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix
  - ROC-AUC Curve

### 5. Deployment
- Save the trained model using joblib or pickle.
- Create a simple Flask or FastAPI application for model inference.
- Deploy on cloud platforms like AWS, GCP, or Heroku.

## Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/yourusername/churn-modelling.git
cd churn-modelling
pip install -r requirements.txt
```

## Usage
Run the Jupyter Notebook for training:
```bash
jupyter notebook Churn_Modelling.ipynb
```

For model inference:
```python
import joblib
model = joblib.load('churn_model.pkl')
prediction = model.predict([[600, 1, 40, 3, 60000, 2, 1, 1, 50000]])
print(prediction)
```

## Contributing
Feel free to contribute by submitting issues or pull requests.

## License
This project is licensed under the MIT License.
