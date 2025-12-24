# Predicting Patient Drug Ratings from Medical Reviews

## Overview
This project builds an NLP regression model to predict patient-reported drug ratings (1–10) using free-text medical reviews and structured metadata.

## Dataset
UCI Drug Reviews (DrugLib): ~4,000 patient reviews including drug name, condition, effectiveness, side effects, and review text.

## Approach
- Combined multiple review text fields into a single document
- TF-IDF vectorization for text features
- Target encoding for high-cardinality categorical variables
- Compared Ridge, ElasticNet, LinearSVR, and SGDRegressor
- Used 5-fold cross-validation for model selection
- Final evaluation on a held-out test set

## Results
- Best model: LinearSVR
- Cross-validation MAE ≈ 1.15
- Test MAE ≈ 1.29
- Strong generalization with minimal overfitting

## Key Takeaways
Text dominates prediction, but structured metadata significantly improves performance.
