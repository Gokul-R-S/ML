# Instant Noodles Demand Forecasting

This repository contains the machine learning-driven solution for optimizing demand forecasting and supply management in the instant noodles distribution business.

## Problem Statement

An FMCG company is facing a critical issue with its instant noodles business due to supply-demand mismatches across different regions:
- **High-demand areas:** Insufficient supply leading to stockouts.
- **Low-demand areas:** Oversupply causing increased inventory costs and waste.

This imbalance leads to financial losses and operational inefficiencies. The goal is to optimize supply quantities across all warehouses.

## Objective

To build a predictive model using historical data to determine the optimal product weight to be shipped to each warehouse.

## Project Workflow

1. **Data Preprocessing:**
   - Handling missing data.
   - Encoding categorical variables.
   - Normalization and scaling of numerical features.

2. **Exploratory Data Analysis (EDA):**
   - Demand trends and seasonality analysis.
   - Regional demand patterns.
   - Warehouse performance metrics.

3. **Feature Engineering:**
   - Creating derived features based on historical demand.
   - Identifying key drivers of demand.

4. **Model Building:**
   - Implementation of regression-based models.
   - Performance comparison across models (e.g., Linear Regression, Random Forest, Gradient Boosting).
   - Hyperparameter tuning to improve accuracy.

5. **Model Evaluation:**
   - Metrics used: R².
   - Analysis of overfitting/underfitting through train-test splits.

6. **Deployment Strategy:**
   - Suggested integration with inventory management systems for real-time demand forecasting.

## Results

- **Performance Metrics:** Achieved a high level of accuracy in predicting optimal shipment quantities, reducing stockouts and oversupply incidents.
- **Business Impact:** Potential for significant cost savings and improved operational efficiency across the supply chain.