# 🍔 Food Delivery Time Prediction
**Machine Learning Project | Regression & Classification**

## 📌 Project Objective
The goal of this project is to predict food delivery durations and categorize delivery status (Fast vs. Delayed) using customer location, restaurant data, weather, and traffic factors. This project demonstrates the application of supervised learning to solve logistical challenges.

## 🛠️ Tech Stack & Environment
- **Environment:** Google Colab
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

## 📂 Project Workflow

### Phase 1: Data Preprocessing & EDA
- **Data Cleaning:** Handled missing values and inconsistencies in columns like `Distance` and `Delivery_Time`.
- **Transformation:** - Encoded categorical variables (Weather, Traffic, Vehicle Type).
  - Normalized continuous features such as `Distance`, `Order_Cost`, and `Order_Time` for consistency.
- **EDA:** - Conducted correlation analysis to identify key predictors.
  - Used Boxplots for **Outlier Detection** in numerical features.

### Phase 2: Predictive Modeling
1. **Linear Regression:** - **Goal:** Predict the exact delivery time in minutes.
   - **Evaluation:** Measured using Mean Squared Error (MSE), R-squared (R²), and Mean Absolute Error (MAE).
2. **Logistic Regression:** - **Goal:** Classify deliveries as "Fast" or "Delayed".
   - **Evaluation:** Measured using Accuracy, Precision, Recall, and Confusion Matrices.

### Phase 3: Visualizations & Insights
- Generated **Scatter Plots** and **Pair Plots** to visualize feature relationships.
- Evaluated classification performance using **ROC Curves** and **Confusion Matrices**.

## 📈 Future Improvements
- **Algorithm Upgrade:** Now that I have completed the basics, I plan to apply **SVM (Support Vector Machines)** to the classification phase to compare its performance against Logistic Regression.
- **Route Optimization:** Integrating distance calculation logic (Haversine formula) for more accurate spatial analysis.
