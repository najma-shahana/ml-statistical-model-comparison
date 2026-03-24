# Breast Cancer Wisconsin (Diagnostic) Dataset

## Source
- scikit-learn built-in dataset
- Originally from the UCI Machine Learning Repository

## Problem Type
- Binary Classification
- Predict whether a tumor is **Malignant** or **Benign** based on cell nucleus features

## Number of Samples
- 569 observations

## Number of Features
- 30 numeric features derived from digitized images of cell nuclei
- Features include mean, standard error, and worst (largest) values of:
  - Radius
  - Texture
  - Perimeter
  - Area
  - Smoothness
  - Compactness
  - Concavity
  - Concave points
  - Symmetry
  - Fractal dimension

## Target Variable
- `target`: Malignant (1) or Benign (0)
- Class distribution:
  - Benign: 357 samples (~63%)
  - Malignant: 212 samples (~37%)

## Notes
- Dataset contains **no missing values**
- Features are **numerical and on different scales**
- Suitable for cross-validation and statistical evaluation
- Can be used with classical ML models like Logistic Regression, SVM, and Random Forest

## References
- Scikit-learn dataset documentation: https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-dataset
- UCI ML Repository: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)
