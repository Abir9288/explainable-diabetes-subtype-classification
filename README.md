# Explainable Multi-Class Subtype Classification of Diabetes

### Comparative Ensemble and Attention-Based Modeling Framework

---

## Abstract

Diabetes is a clinically heterogeneous metabolic disorder comprising multiple subtypes with distinct pathophysiological characteristics. Accurate subtype classification is critical for personalized treatment and improved prognostic outcomes. This project proposes a comparative machine learning framework integrating ensemble-based methods and an attention-enhanced deep neural network for multi-class diabetes subtype classification.

Beyond predictive performance, interpretability is ensured using SHAP (SHapley Additive exPlanations) to identify subtype-specific biomarker contributions. Experimental results demonstrate that gradient-boosting-based ensemble models outperform standalone neural architectures on structured clinical data, while attention mechanisms enhance feature-level representation learning.

---

## 1. Research Objectives

* Perform multi-class classification of diabetes subtypes
* Compare ensemble learning and neural network approaches
* Evaluate models using balanced multi-metric evaluation
* Integrate Explainable AI (XAI) for transparent decision-making
* Identify clinically relevant feature importance patterns

---

## 2. Dataset Description

* **File:** `data/diabetes_dataset00.csv`
* **Type:** Structured clinical tabular dataset
* **Task:** Multi-class subtype classification
* **Features:** Clinical and laboratory biomarkers
* **Target:** Diabetes subtype label

### Preprocessing Pipeline

* Missing value imputation
* Feature normalization / scaling
* Categorical encoding (if applicable)
* Train–test split
* Class imbalance consideration
* Feature consistency validation

---

## 3. Methodology

### 3.1 Ensemble Learning Models

* Random Forest Classifier
* XGBoost Classifier
* CatBoost Classifier
* Voting Ensemble
* Stacking Ensemble

  * Base learners: Tree-based ensemble models
  * Meta-learner: Logistic Regression

### 3.2 Attention-Based Neural Network

A custom neural architecture was implemented including:

* Fully connected dense layers
* Feature-level attention mechanism
* Softmax output for multi-class prediction

The attention module dynamically assigns importance weights to input features, improving subtype discrimination.

---

## 4. Model Evaluation

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* Macro F1-score

### Comparative Performance

Tree-based gradient boosting models achieved the highest overall performance, with XGBoost demonstrating superior accuracy and macro-F1 stability. Stacking ensembles further improved generalization performance. The MLP model exhibited comparatively lower performance, reinforcing the dominance of boosting methods in structured clinical datasets.

---

## 5. Explainability Framework (XAI)

To ensure model transparency:

* Global SHAP summary plots
* Class-wise SHAP analysis
* Feature contribution ranking
* Local prediction explanations

SHAP visualizations are available in:

```
shap_plots/
```

These analyses reveal subtype-specific biomarker importance patterns, enhancing clinical interpretability.

---

## 6. Project Structure

```
explainable-diabetes-subtype-classification/
│
├── data/
│   └── diabetes_dataset00.csv
│
├── code/
│   └── diabetes_dataset.ipynb
│
├── shap_plots/
│   ├── shap_summary.png
│   ├── shap_class_0.png
│   ├── shap_class_1.png
│   └── ...
│
├── results/
│   └── results_comparison.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 7. Reproducibility

Install dependencies:

```
pip install -r requirements.txt
```

Run the notebook:

```
code/diabetes_dataset.ipynb
```

All experiments, model training, evaluation, and SHAP analysis are fully reproducible.

---

## 8. Key Contributions

* Multi-class diabetes subtype modeling
* Comparative evaluation of ensemble and deep learning approaches
* Integration of attention mechanism for tabular data
* SHAP-based explainability for clinical interpretability
* Reproducible research pipeline

---

## 9. Future Work

* External validation on real-world clinical datasets
* Cross-hospital generalization analysis
* Transformer-based tabular architectures
* Deployment as a clinical decision support system
* Statistical significance testing across folds

---

## Author

Md Abir Hossain
Machine Learning & Data Science Researcher
Dhaka Bangladesh

---

## License

This project is intended for academic, research, and educational purposes.
