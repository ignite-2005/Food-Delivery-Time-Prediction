# 🍔 Food Delivery Time Prediction

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange?style=for-the-badge&logo=scikitlearn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter)

# Evolution-Based Machine Learning Workflow for Food Delivery Prediction

A structured machine learning workflow documenting the progression from baseline regression models to tuned classification systems for delivery-time prediction.

</div>

---

# 📌 Overview

This repository documents the development lifecycle of a Food Delivery Time Prediction system using Machine Learning.

The project is organized into chronological evolution phases to demonstrate:
- iterative experimentation
- preprocessing improvements
- feature engineering
- model benchmarking
- hyperparameter optimization

Instead of presenting only a final model, the repository focuses on the engineering and experimentation process behind model development.

---

# 🏗️ Repository Structure

```bash
Food-Delivery-Time-Prediction/
├── evolve_v1/
│   ├── baseline_workflow.ipynb
│   ├── Food_Delivery_Time_Prediction.csv
│   └── README.md
│
├── evolve_v2/
│   ├── advanced_workflow.ipynb
│   └── README.md
│
└── README.md
```

---

# 🗺️ Project Evolution Flow

```mermaid
graph TD
    A[Raw Order Dataset] --> B[Data Cleaning & Preprocessing]
    B --> C[Feature Engineering]
    C --> D[Haversine Distance Calculation]

    subgraph EV1 [Evolution Phase 1 : Baseline Regression]
        D --> E1[Linear Regression]
        D --> E2[Logistic Regression]
        E1 --> F1[Distance Correlation Analysis]
        E2 --> F2[Continuous Variance Evaluation]
    end

    subgraph EV2 [Evolution Phase 2 : Classification & Optimization]
        D --> G1[Gaussian Naive Bayes]
        D --> G2[K-Nearest Neighbors]
        D --> G3[Decision Tree Classifier]
        G2 --> H[GridSearchCV Tuning]
        G3 --> H
        H --> I[Hyperparameter Optimization]
    end

    F1 --> J[Final Comparative Analysis]
    F2 --> J
    I --> J

    style A fill:#1f2937,color:#fff
    style B fill:#2563eb,color:#fff
    style C fill:#7c3aed,color:#fff
    style D fill:#059669,color:#fff
    style J fill:#dc2626,color:#fff
```

---

# 📂 Evolution Phases

## 🔹 evolve_v1 — Baseline Regression Modeling

### Scope
- Initial preprocessing workflow
- Coordinate cleaning
- Exploratory Data Analysis
- Baseline regression implementation

### Implemented Models
- Linear Regression
- Logistic Regression

### Key Observations
- Delivery distance strongly correlates with delivery duration
- High continuous variance impacts regression performance
- Preprocessing quality significantly affects predictions

---

## 🔹 evolve_v2 — Classification & Hyperparameter Tuning

### Scope
- Classification benchmarking
- Hyperparameter optimization
- Cross-validation workflows
- Comparative model evaluation

### Implemented Models
- Gaussian Naive Bayes
- K-Nearest Neighbors
- Decision Tree Classifier

### Optimization Techniques
- GridSearchCV
- Parameter tuning
- Cross-validation

### Key Observations
- Decision Trees improved interpretability
- Tuned KNN achieved improved classification performance
- Hyperparameter optimization significantly affected model accuracy

---

# ⚙️ Machine Learning Workflow

```mermaid
sequenceDiagram
    participant D as Dataset
    participant P as Preprocessing
    participant F as Feature Engineering
    participant M as ML Models
    participant E as Evaluation

    D->>P: Clean Raw Data
    P->>F: Generate Features
    F->>M: Train Models
    M->>E: Evaluate Performance
    E-->>M: Optimize Parameters
```

---

# 📊 Feature Engineering

## 🌍 Haversine Distance

A major engineered feature in this project is the Haversine Distance calculation used to estimate geographical distance between restaurant and customer coordinates.

This feature helps:
- improve spatial understanding
- enhance prediction accuracy
- model real-world delivery conditions more effectively

---

# 🧠 Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-Learn |
| Notebook Environment | Jupyter Notebook |
| Optimization | GridSearchCV |
| Version Control | Git & GitHub |

---

# 📈 Learning Outcomes

This project explores:
- data preprocessing workflows
- regression and classification techniques
- feature engineering
- model benchmarking
- hyperparameter optimization
- comparative evaluation strategies

---