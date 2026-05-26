# Baseline Regression - Preprocessing & Modeling (evolve_v1)

This folder contains the initial version of the food delivery predictive model, focusing on data preprocessing, exploratory data analysis, and baseline regressions.

## 📌 Objectives

1. **Regression**: Predict the exact food delivery duration in minutes (`Delivery_Time`).
2. **Classification**: Categorize delivery status as **"Fast"** or **"Delayed"** based on the median time.

## 📂 Workflow & Data Pipeline

### 1. Data Preprocessing & EDA

- **Data Cleaning**: Resolved inconsistencies and handled missing values in columns like `Distance` and `Delivery_Time`.
- **Feature Engineering**: Converted raw coordinates into distance metrics using the Haversine formula to establish physical constraints.
- **Transformation**:
  - Encoded categorical columns such as `Weather_Conditions`, `Traffic_Conditions`, and `Vehicle_Type`.
  - Normalized continuous features (`Distance`, `Order_Cost`, `Order_Time`) for stable model convergence.
- **EDA**:
  - Analyzed feature correlations to isolate the key drivers of delivery delays.
  - Used boxplots for outlier detection to clean noisy data entries.

### 2. Predictive Modeling

- **Linear Regression (Regression)**:
  - Notebook: [baseline_workflow.ipynb](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v1/baseline_workflow.ipynb)
  - Modeled continuous minutes taken for delivery.
  - Evaluated using Mean Squared Error (MSE), R-squared ($R^2$), and Mean Absolute Error (MAE).
- **Logistic Regression (Classification)**:
  - Classified delivery speed probabilities using the sigmoid activation function.
  - Evaluated using Accuracy, Precision, Recall, and Confusion Matrices.

## 📈 Findings & Takeaways

* **Linear Assumption Limitation**: Linear regression assuming independent additive effects struggled with traffic gridlocks and weather penalties, which affect delivery times non-linearly.
* **Continuous Variance**: Wait times at restaurants and courier delays introduced high variance into continuous minutes prediction, showing that category bounds (Fast vs. Delayed) serve as a more stable operational metric.
