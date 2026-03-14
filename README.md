# 🍔 Food Delivery Time Prediction
**Machine Learning Project | Predictive Analytics & Business Intelligence**

## 📌 Project Objective
The goal of this project is to predict food delivery durations and categorize delivery status (Fast vs. Delayed) using customer location, restaurant data, weather, and traffic factors. This project demonstrates a full-cycle machine learning approach to solving logistical bottlenecks and improving customer satisfaction.

## 🛠️ Tech Stack & Environment
- **Environment:** Google Colab
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

## 📂 Project Workflow

### Phase 1: Data Preprocessing & EDA
- **Data Cleaning:** Handled missing values and inconsistencies in key columns like `Distance` and `Delivery_Time`.
- **Transformation:** - Encoded categorical variables such as `Weather_Conditions`, `Traffic_Conditions`, and `Vehicle_Type`.
  - Normalized continuous features like `Distance`, `Order_Cost`, and `Order_Time` for model consistency.
- **EDA:** - Conducted correlation analysis to identify the most relevant predictors for delivery delays.
  - Used **Boxplots** for Outlier Detection to ensure data quality before training.

### Phase 2: Predictive Modeling
1. **Linear Regression (Regression):**
   - **Goal:** Predict the exact delivery time in minutes.
   - **Evaluation:** Measured using MSE, R-squared (R²), and MAE.
2. **Logistic Regression (Classification):**
   - **Goal:** Classify deliveries as **"Fast"** or **"Delayed"**.
   - **Evaluation:** Evaluated via Accuracy, Precision, Recall, and Confusion Matrices.



### Phase 3: Visualizations & Analysis
- Generated **Scatter Plots** and **Pair Plots** to visualize the relationship between distance, traffic, and time.
- Used **ROC Curves** and **Confusion Matrices** to validate the reliability of the classification model.

---

## 💡 Actionable Insights & Recommendations
Based on the model results, the following operational improvements were identified:

* **Optimizing Delivery Routes:** Implement route optimization logic to minimize costs for both the delivery personnel and the customer. Use Linear Regression results to flag high-risk "long-distance" deliveries for better dispatching.
* **Dynamic Staffing:** Data shows significant delays during rush hours. Recommendations include increasing staffing and optimizing shift scheduling specifically during high-traffic periods.
* **Peak Period Management:** Analysis of the `Order_Time` feature highlights peak delay periods (e.g., evenings). 
* **Incentive Programs:** Strategies to offer bonuses to delivery staff during peak demand times (e.g., Rush Hours, Festival Offers) to maintain service levels.

---

## 📈 Future Improvements
- **Algorithm Upgrade:** Apply **SVM (Support Vector Machines)** to the classification phase to compare performance against Logistic Regression for non-linear delay patterns.
- **Advanced Spatial Analysis:** Integrating the **Haversine formula** for more precise distance calculation based on GPS coordinates.

---
> **Note:** To run this project, ensure `food_delivery_dataset.csv` is uploaded to the same directory as the notebook.
