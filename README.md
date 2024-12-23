# Uber Fare Prediction

## Overview

This project predicts Uber fare prices for future rides using regression analysis. The goal is to enhance customer satisfaction and operational efficiency by providing accurate fare predictions.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling](#modeling)
- [Evaluation Metrics](#evaluation-metrics)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)

## Introduction

The project demonstrates how data-driven techniques can improve fare prediction accuracy, which is essential for ride-hailing platforms. 

## Dataset

The dataset contains 200,000 rows and 9 columns with the following key fields:

- **Key**: Unique trip identifier
- **Fare Amount**: Trip cost in USD
- **Pickup Datetime**: Time when the trip began
- **Passenger Count**: Number of passengers
- **Pickup/Dropoff Longitude/Latitude**: Geographical coordinates of the trip's start and end points

Final processed dataset: **193,481 rows and 10 columns**

## Data Preprocessing

Key steps in preprocessing:
- **Libraries**: NumPy, Pandas, Matplotlib, Seaborn
- **Initial Exploration**: Reviewed column names, data types, and dataset shape
- **Missing Data**: Removed rows with null values
- **Feature Engineering**: Added a distance column using the Haversine formula

## Exploratory Data Analysis (EDA)

- **Distribution Analysis**: Most fares are between $0 and $20, reflecting short or low-cost trips
- **Outlier Removal**: Excluded non-plausible fare and distance values
- **Correlation**: Found a strong positive correlation (0.89) between fare amount and distance

## Modeling

### Model Selection
- **Algorithm**: Random Forest Regression
- **Reason**: Handles both linear and non-linear relationships effectively

### Feature Selection
- The distance feature was identified as a key predictor for fare amounts.

## Evaluation Metrics

- **Mean Absolute Error (MAE)**: 2.32
- **Mean Squared Error (MSE)**: 18.50
- **R² Score**: 0.794 (explains 79.4% of variance in fare amounts)

## Recommendations

1. **Pricing Strategies**:
   - Dynamic pricing for longer rides
   - Loyalty points for frequent short-distance rides
2. **Operational Improvements**:
   - Surge pricing during peak hours
   - Automated outlier detection systems
3. **Customer Experience**:
   - Display predicted fare ranges before trip confirmation
   - Offer shared ride incentives

## Conclusion

The model demonstrates high accuracy and practical applications in predicting Uber fares. Future improvements could include integrating additional features like weather and traffic data.

---

