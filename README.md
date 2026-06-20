# Crop Recommendation Model Comparison

This project builds a crop recommendation classifier from soil and climate measurements. It compares three machine learning models and selects the best performer for crop prediction.

## Project Overview

The model predicts the best crop label using:

- Nitrogen (`N`)
- Phosphorus (`P`)
- Potassium (`K`)
- Temperature
- Humidity
- Soil pH
- Rainfall

## Models Compared

- Logistic Regression
- CatBoost Classifier
- LightGBM Classifier

The notebook trains all models on the same train/test split, evaluates them with multiclass metrics, and uses the best model for the final recommendation.
It also reports feature importance for the best-performing model to show which soil and climate variables drive the recommendations.

## Results

On the current split, CatBoost produced the strongest performance:

| Model | Accuracy | Weighted F1 |
| --- | ---: | ---: |
| CatBoost | 0.9977 | 0.9977 |
| LightGBM | 0.9932 | 0.9932 |
| Logistic Regression | 0.9682 | 0.9681 |

Example field conditions in the notebook produce the recommendation:

```text
coffee
```

## Files

```text
Crop_Recommendation_Model_Comparison.ipynb
data/
  crop_recommendation.csv
README.md
```

## Dataset

Source: Kaggle dataset `ryandinh/agricultural-production-optimization`

The dataset is included locally in:

```text
data/crop_recommendation.csv
```

## How to Run

Install the required Python packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn catboost lightgbm
```

Then open and run:

```text
Crop_Recommendation_Model_Comparison.ipynb
```
