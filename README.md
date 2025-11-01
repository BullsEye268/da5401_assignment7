# DA5401 Assignment 7: Multi-Class Model Selection

**Author:** Achyutha Munimakula PH21B004

## Project Overview

This repository contains the submission for Assignment 7 of the DA5401 course. The objective of this assignment is to perform multi-class model selection for a land cover classification task using the Landsat Satellite dataset from the UCI Machine Learning Repository.

The primary evaluation metrics used are Receiver Operating Characteristic (ROC) curves and Precision-Recall Curves (PRC), adapted for a multi-class problem using the One-vs-Rest (OvR) approach.

## Dataset

The dataset used is the **Statlog (Landsat Satellite)** dataset, which involves classifying land cover types based on multi-spectral satellite image data. It is a multi-class problem with 6 distinct classes.

## Models Compared

A diverse set of classification models were trained and evaluated to compare their performance. The models include:

- K-Nearest Neighbors (KNN)
- Decision Tree Classifier
- Dummy Classifier (as a baseline)
- Logistic Regression
- Gaussian Naive Bayes
- Support Vector Machine (SVC) with probability estimates
- Random Forest Classifier
- XGBoost Classifier
- A custom `PerverseClassifier` (designed to perform poorly for illustrative purposes)

## Results and Conclusion

The models were evaluated based on baseline accuracy/F1-score, Macro-Averaged ROC-AUC, and Macro-Averaged Precision-Recall Average Precision (PRC-AP).

- **Top Performers:** `Random Forest` and `XGBoost` were consistently the best-performing models across all metrics, demonstrating superior discriminative power and a better balance of precision and recall.
- **Final Recommendation:** Based on the comprehensive analysis, **XGBoost** is recommended as the best model for this classification task, with Random Forest being an equally strong alternative.
- **Analysis Insights:** The analysis also highlighted interesting trade-offs, such as the differing performance of `SVC` and `KNN` when evaluated by ROC-AUC versus PRC-AP, underscoring the importance of choosing the right metric for the problem, especially with imbalanced classes.

The complete analysis, code, and visualizations are available in the `submission.ipynb` notebook.
