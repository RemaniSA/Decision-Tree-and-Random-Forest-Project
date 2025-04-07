# Decision Trees and Random Forest Visualisation App

This project was developed as part of the MSc Mathematical Trading and Finance programme at Bayes Business School (formerly Cass). It focuses on building and visualising tree-based classifiers to predict secondary school student performance, with an interactive Python Shiny app for non-technical users to explore hyperparameter tuning, overfitting, and feature importance.

## Problem

The objective was to create an interpretable classification system using decision trees and random forests on a public education dataset. Final grades (G3) were predicted using a range of social, demographic, and academic inputs. The emphasis was placed on not only achieving robust model performance, but also making the logic of these models accessible to a non-technical audience.

## My Reflections

The construction of this app sharpened my understanding of the trade-off between model complexity and interpretability. Many people use the term 'blackbox' to describe ML models, but this project reinforced that even complex models can offer meaningful insights, provided you have the right tools. We used SHAP values to expose how features contributed to predictions, and the app allowed users to see how models evolved with different hyperparameters. Watching trees grow and observing when they started to overfit was especially enlightening. Overfitting isn’t just a high train accuracy stat; it's a visual cue that your model is learning the noise. If time had allowed, we would have added boundary visualisations and a magnifier feature to better support ensemble method interpretability.

## Methods

- Preprocessing: One-hot encoding, outlier filtering, categorical feature simplification
- Classification Models: Decision Tree, Random Forest (both with GridSearchCV tuning)
- Evaluation Metrics: Accuracy, Weighted F1, ROC curves
- Interpretability: SHAP values, depth pruning, feature importance charts

## Interactive App Features

The Shiny app allows users to:

- Toggle between Decision Tree and Random Forest models
- Adjust hyperparameters in real-time (max depth, α, number of estimators)
- Compare training vs test accuracy interactively
- Explore SHAP values and tree structure visualisations

## Repository Structure

```
Decision-Tree-and-Random-Forest-Project/
├── datasets/
├── .gitignore
├── Decision Tree and Random Forest for Student Performance Prediction.pdf
├── README.md
├── Task.jpg
├── Task.pdf
├── app.py
├── requirements.txt
├── student_performance.py
```

## Summary of Results

| Model           | Cross-Validation Accuracy | Test Accuracy | Comments                         |
|----------------|---------------------------|---------------|----------------------------------|
| Decision Tree  | 70.1%                     | 72.27%        | Best generalisation performance  |
| Random Forest  | 72.7%                     | 66.39%        | Higher variance; prone to overfit|

> ROC curves and SHAP values confirm that the Decision Tree model generalised more consistently. Absences and family support emerged as key features.

## Requirements

```bash
pip install -r requirements.txt
```

See `requirements.txt` for exact versions.

## How to Run

Clone the repository and launch the model or app:

```bash
git clone https://github.com/RemaniSA/Decision-Tree-and-Random-Forest-Project.git
cd Decision-Tree-and-Random-Forest-Project
```

To run the Shiny app:

```bash
cd app/
shiny run --reload app.py
```

## Further Reading

- Géron, A.: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*
- Lundberg & Lee (2017): *A Unified Approach to Interpreting Model Predictions (SHAP)*

## Authors

- Shaan Ali Remani  
- José Pedro Pessoa Dos Santos  
- Chin-Lan Chen  
- Poh Har Yap

---

### Connect

- [LinkedIn](https://www.linkedin.com/in/shaan-ali-remani)  
- [GitHub](https://github.com/RemaniSA)
