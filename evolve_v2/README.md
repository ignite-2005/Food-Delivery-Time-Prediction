# Advanced Classification Benchmarking (evolve_v2)

This folder contains the second version of the food delivery predictive model, benchmarking multiple classification architectures and optimizing hyperparameters via GridSearchCV.

## 📌 Objectives
Classify deliveries into **Fast (0)** vs. **Delayed (1)** categories to compare predictive capabilities and select the optimal model for dispatch decisions.

## 📂 Workflow & Optimization

### 1. Classifier Implementations
- **Gaussian Naive Bayes (GNB)**:
  - Probabilistic model calculating classes under the conditional independence assumption.
  - *Takeaway*: Performance is limited because features like weather and traffic are naturally correlated, violating GNB's core assumption.
- **K-Nearest Neighbors (KNN)**:
  - Classifies delivery instances based on geographical and timing neighborhoods.
  - *Tuning*: GridSearchCV swept $k \in [1, 14]$ to find the optimal neighbor threshold ($k=7$).
- **Decision Tree Classifier**:
  - Notebook: [advanced_workflow.ipynb](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v2/advanced_workflow.ipynb)
  - Recursively splits features by Gini Impurity to construct hierarchical decisions.
  - *Tuning*: GridSearchCV tuned `max_depth` and `min_samples_split` to prune branches and mitigate overfitting.

### 2. Model Performance Evaluation
Models were benchmarked using classification reports, confusion matrices, and ROC-AUC curve profiles:

* **Decision Tree (Recommended)**: ROC-AUC: **0.92**, Accuracy: **89.6%**
* **K-Nearest Neighbors**: ROC-AUC: **0.88**, Accuracy: **85.2%**
* **Gaussian Naive Bayes**: ROC-AUC: **0.81**, Accuracy: **78.5%**

## 💡 Operational Recommendations
* **Dynamic ETAs**: Use the Decision Tree to automatically flag orders under delayed conditions (e.g. rush-hour rain) and add a buffer to customer ETAs beforehand.
* **Inclement Weather Radius Capping**: Dynamically shrink maximum delivery radius zones during weather alerts to prevent long-distance delivery delays.
