---
layout: page
title: "Customer Churn Prediction & Analytics"
description: Built ML models on 7,000+ records to predict customer churn with 90% accuracy and proposed strategies for 15% churn reduction.
img: assets/img/5.jpg
importance: 1
category: Academic
---

## Overview

Led a comprehensive customer churn analysis project to identify key drivers of customer attrition and build predictive models that enable proactive retention strategies. The project combined rigorous statistical analysis with practical business recommendations.

## Challenge

A telecom company needed to understand why customers were leaving and identify at-risk customers before they churned. The dataset contained **7,000+ customer records** with significant class imbalance — churned customers represented a minority of the population.

## Approach

- **Data Preprocessing:** Cleaned and engineered features from raw customer data. Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to address the class imbalance problem.
- **Model Development:** Developed and compared three predictive models — **Logistic Regression**, **Random Forest**, and **XGBoost** — with systematic hyperparameter tuning and cross-validation.
- **Feature Importance:** Used **SHAP** (SHapley Additive exPlanations) to identify the most influential churn drivers, including contract length, monthly charges, and service response time.
- **Visualization & Reporting:** Created interactive visual reports using **Tableau** to communicate churn drivers and proposed retention strategies to stakeholders.

## Results

| Metric | Value |
|--------|-------|
| Best model accuracy | **90%** (XGBoost, AUC=0.89) |
| Projected churn reduction | **15%** |
| Key drivers identified | Contract length, monthly charges, service response time |

## Tech Stack

`Python` · `Scikit-learn` · `XGBoost` · `SMOTE` · `SHAP` · `Tableau` · `Pandas`
