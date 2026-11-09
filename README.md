# Student Performance Prediction System

## Problem
The prototype explores whether historical student information can help identify learners who may need additional academic support.

## Dataset
UCI Student Performance Dataset: https://archive.ics.uci.edu/dataset/320/student+performance

## Prediction target
- `G3 < 10`: `AT RISK`
- `G3 >= 10`: `NOT AT RISK`

`G3` is the target only. It is excluded from the model input features to prevent target leakage.

## Technologies
Python, pandas, scikit-learn, Random Forest, Streamlit, joblib, ucimlrepo, and GitHub.

## Installation
Use Python 3.10 or later. Open a terminal in this project folder and run:

```bash
pip install -r requirements.txt
```

## Train the model
```bash
python train_model.py
```

This downloads the UCI dataset, creates `student_data.csv`, trains and evaluates the Random Forest classifier, and saves `student_model.pkl`.

## Run the application
```bash
streamlit run app.py
```

Open the local address printed in the terminal (normally http://localhost:8501). Download the sample input CSV from the app, upload it, and review the predictions.

## Limitations
This is a classroom demonstration using public historical data. The model was trained on one Portuguese secondary-school dataset and may not generalize to another school or population. Predictions are not diagnoses and must not be the sole basis for real student decisions. Faculty should review a prediction and provide appropriate support.
