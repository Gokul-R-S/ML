# Delivery Status Prediction Model

## Project Overview
This project focuses on developing a predictive model to classify the delivery status of orders in the supply chain domain, addressing challenges related to delivery delays. By leveraging historical data, the model identifies key factors affecting delivery outcomes and provides actionable insights to enhance operational efficiency and customer satisfaction.

---

## Business Problem
The goal is to predict delivery delays in supply chain management to minimize disruptions and costs. Using historical delivery data, the model aims to:
- Classify delivery status (successful or delayed).
- Enable proactive management of potential delays.
- Enhance overall supply chain efficiency.

---

## Dataset Details
### Features
- **Numerical Features (7):**
  - Sales, Price, Profit Ratio, Discount, Order Profit
  - Product Length, Product Weight
- **Categorical Features (16):**
  - **Customer-related:** Category, State
  - **Order-related:** Zone, Transaction, Status (Target variable)
  - **Product-related:** Type, Category, Dept Name
  - **Shipping-related:** Class, Scheduled, Dispatched
  - **Logistics-related:** Warehouse Region
  - **Time-related:** Session, Weekday Order
  - **Others:** Quantity, Delivery Review

### Preprocessing
- **Duplicate Rows:** None found.
- **Redundant Features:**
  - Removed `Order ID`, `Customer ID`, `Product Category ID`, `Zip Code`, and `Dept ID`.
- **Null Value Imputation:**
  - Numerical features: Mean (normal distribution) or median (skewed distribution).
  - Categorical features: Mode.

---

## Exploratory Data Analysis
### Key Findings
- **Statistical Tests:**
  - Significant differences observed for `Product Length` (T-Test) and associations with `Transaction`, `Product Type`, `Shipping Class`, `Scheduled Shipping`, and `Delivery Status` (Chi-Square Test).
  - Non-normal distributions identified for all numerical features (Shapiro Test).
- **Multicollinearity:**
  - Highest VIF = 6.52 (`Price`), below the threshold of 10.

### Feature Engineering
- **Transformations:**
  - Yeo-Johnson transformation applied to `Sales`, `Price`, `Profit Ratio`, `Order Profit`, `Product Weight`.
- **Encoding:**
  - Techniques: One-Hot, CatBoost, Ordinal, and Binary Encoding.

---

## Model Development
### Techniques
- **Baseline Models:** Logistic Regression, LightGBM, XGBoost.
- **Handling Imbalance:** SMOTE improved recall slightly but was limited by dataset noise.
- **Hyperparameter Tuning:** GridSearchCV enhanced model performance (e.g., LightGBM, CatBoost).
- **Stacking:** Combined multiple models to improve metrics but introduced risks of overfitting.

### Performance
- **Best Model:** LightGBM with SMOTE and hyperparameter tuning.
  - **Metrics:** Recall = 0.93, Accuracy = 0.75.
- **Stacking Model:** Demonstrated potential for higher accuracy by leveraging diverse strengths.

---

## Reflections and Future Scope
### Reflections
- Accurate predictions support proactive interventions and operational efficiency.
- Data quality was a key limitation, affecting reliability and insights.

### Future Improvements
- Integrate external factors (e.g., traffic, weather) for better insights.
- Enhance feature richness through advanced engineering and real-time data.
- Improve data quality to sustain interpretability and performance.

