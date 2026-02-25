## Project Summary -
   This project aims to improve Customer Satisfaction (CSAT) by using Machine Learning techniques on customer support data. I performed data cleaning and Exploratory Data Analysis (EDA) to identify key factors affecting customer experience. To handle class imbalance, SMOTE was applied, and a Random Forest Classifier was trained to predict CSAT scores effectively.
   
## Business Context -
In the highly competitive e-commerce sector, Customer Satisfaction (CSAT) is a key performance metric for Flipkart. This project analyzes customer support interactions to identify key drivers of satisfaction and dissatisfaction. It also helps in predicting CSAT scores to proactively identify at-risk customers and improve overall support experience.

## Problem Statement -
Customer support teams often work reactively, identifying unhappy customers only after negative feedback or churn. Manually analyzing large volumes of support data is inefficient, and class imbalance makes it difficult for models to detect low CSAT cases. This project solves this by building a machine learning model to predict CSAT scores and using GenAI to summarize customer complaints for faster insights.

## Technical Architecture

The project follows a structured data science lifecycle:

Data Preprocessing:

Handled missing values using appropriate strategies (e.g., median/mode imputation)

Converted timestamp features to extract meaningful metrics like response and resolution time

Treated outliers in key numerical features (e.g., handling time) by capping extreme values

Exploratory Data Analysis (EDA):

Identified strong class imbalance (majority of ratings are 5-star)

Observed that higher handling time leads to lower CSAT scores (negative correlation)

Analyzed distribution of ratings and key feature relationships

Feature Engineering:

Created Response_Time_Min (time taken to respond to customer)

Derived additional time-based and interaction-based features

Applied One-Hot Encoding for categorical variables (e.g., Channel, Issue Type)

Imbalance Handling:

Applied SMOTE (Synthetic Minority Oversampling Technique)

Balanced minority classes (low CSAT scores) to improve model learning

Training data increased significantly after resampling

Model Implementation:

Algorithm Used: Random Forest Classifier

Chosen for its robustness, ability to handle non-linear data, and feature importance insights

Model Evaluation:

Evaluated using Precision, Recall, F1-score, and Accuracy

Found model performs well on majority class but struggles with minority classes

Highlighted need for further imbalance handling and tuning

## Key Business Insight:
👉 The most important factor affecting Customer Satisfaction is: response_time_min

💡 Recommendation:
Focus on optimizing 'response_time_min' to improve overall CSAT scores.
This feature has the highest impact on customer experience.