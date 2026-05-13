# Intelligent Intrusion Detection System

This repository contains a machine learning pipeline for intrusion detection using the CICIDS2017-style dataset.

## Contents

- `p/all.ipynb` - Main notebook with data loading, preprocessing, model training, evaluation, and a Gradio interface.
- `p/xgb_dos_model.pkl` - Saved XGBoost model.
- `p/rfc_dos_model.pkl` - Saved Random Forest model.
- `p/lr_dos_model.pkl` - Saved Logistic Regression model.
- `p/MachineLearningCVE/` - Dataset CSV files used for training and testing.

## Features

- Dataset loading and concatenation from multiple CSV files
- Data cleaning and NaN/infinity handling
- Label encoding and class balancing
- Feature selection using XGBoost importance and correlation filtering
- Training and evaluation of XGBoost, Random Forest, and Logistic Regression models
- Gradio-based prediction interface with optional LLM explanation support

## How to Run

1. Open `p/all.ipynb` in Jupyter or VS Code.
2. Install required packages if needed:
   ```bash
   pip install pandas numpy scikit-learn xgboost matplotlib seaborn gradio google-genai
   ```
3. Run the notebook cells sequentially.
4. If using the Gradio interface, set `GOOGLE_GENAI_API_KEY` in your environment to enable Gemini explanations.

## Notes

- The Gradio interface currently launches with `share=False`, `inbrowser=False`, and `inline=False` to avoid notebook frame restrictions.
- The notebook includes fallback handling for missing Gemini API keys and connection errors.
- Existing data and model artifacts are stored under `p/`.

