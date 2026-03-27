# Statistical Comparison of Machine Learning Models

**Author:** Najma Shahana M H  

**Date:** 25 January 2026

## Overview

This project examines how statistical methods can be used to evaluate and compare machine learning models in a more reliable way. Instead of relying on a single train–test split, the analysis focuses on how model performance varies across different samples of the data.

The work is carried out on the Breast Cancer Wisconsin (Diagnostic) dataset, with an emphasis on combining concepts from **machine learning and applied statistics**.

---

## Motivation

In many introductory machine learning workflows, models are compared using a single performance score. However, such comparisons can be misleading, as they do not account for variability due to different data splits.

As a student of applied statistics, this project was undertaken to explore:
- how performance changes across multiple samples,
- how to quantify uncertainty in model evaluation, and
- how statistical tests can be used to compare models more rigorously.

---

## Dataset

- **Dataset:** Breast Cancer Wisconsin (Diagnostic)  
- **Number of observations:** 569  
- **Number of features:** 30 numerical variables  
- **Target variable:**  
  - 0 → Benign  
  - 1 → Malignant  

The dataset is clean (no missing values) and suitable for classical classification models.

A detailed description is provided in:  
`data/dataset_description.md`

---

## Models Considered

The following models were used:

- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)  

These models were selected to represent different approaches:
- a linear statistical model,
- a tree-based ensemble method, and
- a margin-based classifier.

---

## Methodology

### Cross-Validation

A **5-fold stratified cross-validation** approach was used.  
This ensures that each fold maintains the class distribution of the dataset, while also allowing every observation to be used for both training and testing.

### Performance Metrics

Model performance was evaluated using:
- **Accuracy**
- **ROC-AUC**

Rather than reporting a single value, metrics were recorded for each fold to study variability.

---

## Statistical Analysis

To better understand model performance, the following were computed:

- Mean and standard deviation of metrics across folds  
- Approximate **95% confidence intervals**  
- **Wilcoxon signed-rank test** for pairwise comparison  

This approach treats fold-wise results as paired observations and allows for a more meaningful comparison between models.

---

## Results and Discussion

Both Logistic Regression and Random Forest achieved high performance across all folds. While Random Forest showed slightly higher accuracy in some cases, the differences between the two models were small and not consistent across all folds.

Logistic Regression, on the other hand, showed more stable performance, with less variation between folds. This suggests that, for this dataset, a simpler linear model can perform competitively with more complex methods.

The SVM model showed comparatively lower accuracy and greater variability, indicating that it may require additional tuning or preprocessing to perform optimally.

Overall, the results highlight that small differences in average performance should be interpreted with caution, especially when variability is taken into account.

---

## Key Takeaways

- Model evaluation should consider variability, not just average performance  
- Cross-validation provides a more reliable estimate of model behavior  
- Statistical testing helps determine whether differences are meaningful  
- Simpler models can perform well on structured datasets  

---

## Project Structure
ml-statistical-model-comparison/
│
├── data/
│ └── dataset_description.md
│
├── notebooks/
│ └── model_comparison.ipynb
│
├── results/
│ └── metrics_tables.csv
│
└── README.md

---

## Tools and Libraries

- Python  
- scikit-learn  
- pandas, numpy  
- scipy  
- matplotlib, seaborn  

---

## Limitations

- The analysis is based on a single dataset  
- Only three models were considered  
- Hyperparameter tuning was limited  
- Results may not generalize to other domains  

---

## Author

Najma Shahana M H  
M.Sc. Applied Statistics (IGNOU)  

---

## Conclusion

This project demonstrates how statistical thinking can improve the way machine learning models are evaluated. By focusing on variability and significance rather than single-point estimates, it is possible to arrive at more reliable and interpretable conclusions.
