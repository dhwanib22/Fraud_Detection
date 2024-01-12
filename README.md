# Fraud Detection

## Overview

This project aims to develop a robust machine learning model to effectively detect fraudulent transactions in a payment gateway system. The goal is to minimize financial losses for vendors and customers while ensuring a seamless checkout experience.

## Problem Statement

IndAvenue, a payment gateway startup, is facing challenges due to a lack of a strong fraud detection system. This has resulted in significant financial burdens for vendors and customer churn. The objective is to create a machine learning model that accurately predicts fraudulent transactions and provides actionable recommendations for implementation.

## Dataset Description

- **Target Attribute:** "is_fraud" (discrete variable: 2 classes)
- **Files:**
  - `train_data.csv`: Contains unique transaction numbers, associated "is_fraud" labels, and various transaction features.
  - `test_data.csv`: Similar to `train_data.csv` without the target column.
  - `Solution.csv`: Use this file to evaluate the model output on the test data.

## Project Tasks

### Exploratory Analysis

Explore the dataset using visualizations and numerical analysis to derive insights and patterns. Identify the impact of important attributes on the target variable.

### ML Modelling

Create a robust fraud detection framework by engineering new features, tuning, and improving baseline ML model performance. Evaluate the model using the F1 Score.

### Recommendations and Implementation Strategies

Provide recommendations to IndAvenue and suggest implementation strategies based on your findings.

## Model Performance

- **Decision Tree:**
  - R-squared error: 0.82
  - F1 Score: 90.91%

## Recommendations to the Business

1. **Unified Payment Services (UPI):**
   - UPI shows no fraud, making it a suitable option for smaller transactions.

2. **Visa/Master Debit Cards:**
   - Consider limiting transactions to Visa/Master Debit cards for amounts beyond 25k, especially under 50k.

3. **Partnerships:**
   - Discontinue partnerships (e.g., 39445, 71001, 173558) with less than 100 transactions resulting in fraud.

4. **Categories:**
   - Focus on fraud prevention in categories 1, 2, 3, and 8.

5. **Money Transacted Bins:**
   - Categorize transactions based on the amount to identify low, moderate, and high-risk ranges.


### Explanation of ML Model (Non-technical)

The used model is a Decision Tree Classifier, a type of supervised learning for classification. It builds a tree structure where nodes represent conditions on features, and leaves represent the predicted class. The model incrementally develops the tree by dividing the dataset into subsets based on conditions.

### Strategies for Fast Customer Checkout

1. **Payloud Payment Boxes:**
   - Use automated systems to announce successful payments, ensuring quick customer feedback.

2. **Payment Bins Handling:**
   - Implement separate queues for red, yellow, and green payment bins, with enhanced security checks for higher-risk transactions.

3. **Encourage UPI Usage:**
   - Promote UPI usage for smaller transactions (green category) due to reported safety and speed.

4. **Stable Internet Connection:**
   - Ensure a stable internet connection to prevent transaction glitches and ensure successful processing.

