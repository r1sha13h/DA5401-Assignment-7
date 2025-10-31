# Soil Classification using Machine Learning

A comprehensive multi-class classification project analyzing Statlog Landsat Satellite data to classify 6 different soil types using various machine learning algorithms with detailed performance evaluation through ROC and Precision-Recall curves.

## Project Overview

This project implements and compares 9 different classification models on satellite imagery data to distinguish between:
- Red soil
- Cotton crop
- Grey soil
- Damp grey soil
- Soil with vegetation stubble
- Very damp grey soil

## Key Features

- **Multi-class Classification**: 6-class soil type classification from satellite spectral data
- **Comprehensive Model Comparison**: 9 models including ensemble methods, linear models, and baseline classifiers
- **Advanced Evaluation Metrics**: ROC curves, Precision-Recall curves, confusion matrices
- **Dimensionality Reduction**: PCA analysis for visualization and feature reduction
- **Decision Boundary Visualization**: 2D projections showing model behavior

## Models Implemented

1. **XGBoost** (Best performer: 91.9% accuracy)
2. **Random Forest** (91.1% accuracy)
3. **Support Vector Classifier (SVC)** (90.8% accuracy)
4. **K-Nearest Neighbors (KNN)** (89.9% accuracy)
5. **Decision Tree** (85.1% accuracy)
6. **Logistic Regression** (82.8% accuracy)
7. **Gaussian Naive Bayes** (80.4% accuracy)
8. **Dummy Classifier** (Baseline)
9. **Bad Classifier** (Anti-baseline for comparison)

## Dataset

- **Source**: Statlog Landsat Satellite Dataset
- **Samples**: 6,442 instances
- **Features**: ~36 spectral bands
- **Classes**: 6 soil types (moderately balanced)
- **Split**: 80% training, 20% testing

## Results Summary

### Top Performers
- **XGBoost**: 91.9% accuracy, 0.993 ROC AUC
- **Random Forest**: 91.1% accuracy, 0.991 ROC AUC
- **SVC**: 90.8% accuracy, 0.989 ROC AUC

### Key Insights
- Ensemble methods significantly outperform traditional algorithms
- First 2 PCA components capture 85.2% of variance
- Damp grey soil variants show natural confusion due to spectral similarity
- Models achieve strong macro-averaged performance across all classes

## Visualizations

The project includes:
- **Class Distribution**: Bar charts showing dataset balance
- **PCA Variance Analysis**: Component-wise and cumulative variance plots
- **Decision Boundaries**: 2D projections of model classification regions
- **Confusion Matrices**: Per-model error analysis
- **ROC Curves**: One-vs-Rest macro-averaged curves
- **Precision-Recall Curves**: Class-specific performance evaluation

## Analysis Highlights

### Part A: Data Preparation & Baseline
- Data loading and preprocessing with StandardScaler
- Train-test split (80-20)
- PCA analysis revealing strong dimensionality reduction potential
- Baseline model training and evaluation

### Part B: ROC Analysis
- One-vs-Rest (OvR) approach for multi-class ROC curves
- Macro-averaged AUC calculation
- Identification of XGBoost as best discriminator (AUC = 0.993)
- Bad Classifier demonstrates AUC < 0.5 (systematic misclassification)

### Part C: Precision-Recall Analysis
- Focus on minority class performance
- Average Precision (AP) scores for each model
- Comparison with random baseline (AP = 0.167)
- Demonstrates robustness of ensemble methods

## Contributing

This is an academic project for IIT Madras DA Lab Assignment 7. Feedback and suggestions are welcome.

## License

This project is part of academic coursework at IIT Madras.

## Author

Rishabh Mishra - IIT Madras
