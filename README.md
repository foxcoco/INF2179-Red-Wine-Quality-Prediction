# Red Wine Quality Prediction

A machine learning project comparing Decision Tree, Logistic Regression, and Random Forest models to predict wine quality based on physicochemical properties. The Random Forest model achieved the best performance with **82.2% accuracy** and **0.91 AUC-ROC**.

## Key Results

| Model | Accuracy | Precision | Recall | F1 Score | AUC |
|---|---|---|---|---|---|
| Decision Tree | 0.756 | 0.773 | 0.773 | 0.773 | 0.80 |
| Logistic Regression | 0.747 | 0.769 | 0.756 | 0.762 | 0.83 |
| **Random Forest** | **0.822** | **0.836** | **0.831** | **0.834** | **0.91** |

## Top Predictive Features (Random Forest)

1. **Alcohol** (18.3%) — strongest predictor of wine quality
2. **Sulphates** (13.7%) — second most important feature
3. **Volatile Acidity** (11.3%) — negatively correlated with quality

## Methods

- **Data Preprocessing**: MinMax normalization, binary classification (quality > 5 → "High", else → "Low")
- **Hyperparameter Tuning**: GridSearchCV with 5-fold cross-validation for all three models
- **Evaluation**: Accuracy, Precision, Recall, F1 Score, ROC-AUC, Confusion Matrix
- **Explainability**: Feature Importance, Individual Conditional Expectation (ICE) plots, Partial Dependence Plots (PDP)

## Tech Stack

- **Python 3** — Pandas, NumPy, Matplotlib, Seaborn
- **Machine Learning** — scikit-learn (DecisionTreeClassifier, RandomForestClassifier, LogisticRegression, GridSearchCV)
- **Preprocessing** — MinMaxScaler, train_test_split

## Dataset

Source: [UCI Machine Learning Repository — Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/wine+quality)

The dataset contains **1,599 red wine samples** with 11 physicochemical input features (e.g., acidity, sugar, pH, alcohol) and one output variable (quality score 0–10).

To use this project, download `winequality-red.csv` from the UCI repository and place it in the `data/` directory.

## Project Structure

```
├── README.md
├── data/
│   └── (place winequality-red.csv here)
├── notebook/
│   └── red_wine_quality_prediction.ipynb
└── report/
    └── Red_Wine_Quality_Prediction_Report.pdf
```

## Contributions

This was a four-person project completed during my Master's program at the University of Toronto. My primary contributions included:

- Exploratory data analysis and visualization (box plots, correlation heatmap, violin plots)
- Data preprocessing pipeline (normalization, binary classification encoding)
- Model evaluation and comparison (metrics tables, ROC curves)
- Feature importance analysis and interpretation

## License

This project uses the publicly available Wine Quality Dataset from the UCI ML Repository. The analysis is provided for educational and research purposes.
