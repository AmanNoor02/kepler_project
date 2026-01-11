# Kepler Exoplanet Candidate Classification

## Overview
This project uses the NASA Kepler cumulative dataset to classify Kepler Objects of Interest (KOIs) as:
- CANDIDATE
- CONFIRMED
- FALSE POSITIVE

It is a multi-class supervised learning problem using astronomical features.

## Dataset
- Kepler cumulative dataset (`cumulative.csv`)
- Source: Kaggle / NASA Exoplanet Archive

## Features
- koi_period, koi_prad, koi_depth, koi_srad, koi_steff, koi_slogg

Target:
- koi_disposition

## Models Tried
- Logistic Regression (baseline + balanced)
- Decision Tree
- Random Forest
- Tuned Random Forest (RandomizedSearchCV)

## Best Result
- Tuned Random Forest: ~0.693 accuracy on the held-out test set
- Strong CONFIRMED recall (~0.75)
- CANDIDATE is the hardest class due to ambiguity in signals

## How to Run
1. Create an environment and install dependencies:
   - `pip install -r requirements.txt`
2. Open the notebook in Jupyter and run all cells:
   - `notebooks/kepler_classification.ipynb`