# Predicting Credit Card Consumption for a Leading Bank

## 🧠 Objective
To build a predictive model that estimates average credit card consumption for the next three months (July, August, September) using demographic and behavioral data of bank customers.

## 📄 Overview
Credit card usage behavior is an essential indicator for banking and marketing strategies. Understanding how customer characteristics relate to credit card consumption can empower the bank to create personalized campaigns, reduce churn, and increase profitability.

This project utilizes historical credit and debit transaction data, personal demographics, loan activities, and investment behavior to predict future credit card spending.

## 📦 Dataset Used
1. <a href="https://github.com/SourabhaSekharRout/Predict-Credit-Consumption-of-Customer-For-Leading-Bank/blob/main/CustomerDemographics.xlsx">CustomerDemographics</a>
– Includes account details, customer demographic features, tenure, and digital behavior.
2. <a href="https://github.com/SourabhaSekharRout/Predict-Credit-Consumption-of-Customer-For-Leading-Bank/blob/main/CustomerBehaviorData.xlsx">CustomerBehaviorData</a>
– Contains transactional and financial product behavior including card usage, loan activities, and investments.
3. <a href="https://github.com/SourabhaSekharRout/Predict-Credit-Consumption-of-Customer-For-Leading-Bank/blob/main/CreditConsumptionData.xlsx">CreditConsumptionData</a>
– Contains the target variable `cc_cons`, which is the average credit card consumption in the upcoming 3 months.

## ❓ Questions Addressed
- Which customer demographics and behaviors influence credit card consumption?
- What are the strongest predictors of future credit consumption?
- Can we accurately forecast average credit card usage for customers with missing target values?

## 🔁 Process

### 1. Data Import
- Load all datasets using Python libraries like `pandas`, `numpy`, and `os`.

### 2. Data Audit
- Inspect dataset dimensions, data types, and null values.
- Identify potential issues such as inconsistencies, duplicates, or irrelevant features.

### 3. Data Cleaning
- Rename columns using consistent naming conventions (e.g., lowercase, underscores).
- Convert appropriate columns to categorical/numeric types.
- Impute missing values using domain knowledge or statistical methods.
- Remove duplicates and treat outliers via capping or transformation.

### 4. Data Merge
- Merge the three datasets on the common `ID` column to create a consolidated modeling dataset.

### 5. Exploratory Data Analysis (EDA)
- **Univariate Analysis**: Distribution plots, value counts, and summary statistics for individual variables.
- **Bivariate Analysis**: Scatter plots, boxplots, and correlation matrices to examine relationships between predictors and `cc_cons`.

### 6. Data Modeling
- Feature engineering: Create meaningful variables from transactional data.
- Model training using **Random Forest Regressor**.
- Validate predictions using **Root Mean Square Percentage Error (RMSPE)**.
- Fine-tune hyperparameters and assess feature importance.

## 🧩 Features
- Demographic info: gender, age, income, region, etc.
- Behavior: monthly CC/DC transactions, loan inquiries, investments, EMI payments.
- Transactional stats: debit/credit count and amount over 3 months.
- Account usage: net banking, average transaction interval.

## 💡 Key Insights
- Customers with higher income and longer tenure tend to spend more via credit cards.
- A higher number of credit card transactions is strongly correlated with future spending.
- Active loans and investment activities are significant predictors of card usage.
- Average days between transactions can be a proxy for engagement and credit utilization.

## 📈 Outputs
- A trained random forest model with optimized RMSPE.
- A CSV file with predicted `cc_cons` values for customers where the target was missing.

---

> **Note**: Model performance is measured using RMSPE to handle the variability and scale of spending amounts accurately.
