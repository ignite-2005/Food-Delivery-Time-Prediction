# Food Delivery Time Prediction

This repository contains notebooks and documentation for analyzing and predicting food delivery times. The project is structured sequentially into chronological version directories to show progression from baseline models to hyperparameter-tuned classifiers.

---

## 📁 Repository Structure

The files are organized into sequential version folders:

```directory
Food-Delivery-Time-Prediction/
├── evolve_v1/
│   ├── baseline_workflow.ipynb                   # Preprocessing & baseline regression models (Version 1)
│   ├── Food_Delivery_Time_Prediction.csv         # Raw delivery order dataset
│   └── README.md                                 # Baseline regression details & EDA
├── evolve_v2/
│   ├── advanced_workflow.ipynb                   # Classification benchmarking & hyperparameter tuning (Version 2)
│   └── README.md                                 # Tuned classification benchmarks & GridSearchCV results
└── README.md                                      # Repository project overview
```

---

## 🗺️ Project Progression Flowchart

```mermaid
graph TD
    A["Raw Order Data"] --> B["Data Preprocessing"]
    B --> C["Feature Engineering: Haversine Distance"]
    
    subgraph v1_sub ["Version 1: Baseline Regression (evolve_v1)"]
        C --> D1["Linear Regression"]
        C --> D2["Logistic Regression"]
        D1 --> E1["Findings: Distance correlation & high continuous variance"]
    end

    subgraph v2_sub ["Version 2: Classification & Tuning (evolve_v2)"]
        C --> F1["Gaussian Naive Bayes"]
        C --> F2["K-Nearest Neighbors"]
        C --> F3["Decision Tree Classifier"]
        F2 --> G["GridSearchCV Tuning"]
        F3 --> G
        G --> H["Findings: Tree splits & GridSearchCV optimal parameters"]
    end

    E1 --> I["Summary & Operational Recommendations"]
    H --> I
```

---

## 🔬 Subfolder Documentation & Notebooks

Detailed information on the preprocessing, models, and findings for each phase is documented inside the version folders:

1. **[evolve_v1/](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v1)**: Baseline Regression Modeling & Coordinates Preprocessing.
   - Notebook: [baseline_workflow.ipynb](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v1/baseline_workflow.ipynb)
   - Phase Document: [evolve_v1/README.md](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v1/README.md)
2. **[evolve_v2/](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v2)**: Advanced Classification Benchmarking & Hyperparameter Tuning.
   - Notebook: [advanced_workflow.ipynb](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v2/advanced_workflow.ipynb)
   - Phase Document: [evolve_v2/README.md](file:///c:/Users/admin/VSCode/ML/Food-Delivery-Time-Prediction/evolve_v2/README.md)
