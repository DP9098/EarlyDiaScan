# EarlyDiaScan
To detect early-stage diabetes risk using user inputs like symptoms and demographics, powered by a Machine Learning model (XGBoost) integrated into a Flask web app.

# Core Features:
## 1. User Input Form:
  Inputs: Age group, Polyuria, Polydipsia, Sudden Weight Loss, etc.  
  Also includes name, mobile number, and email for saving reports.
## 2. Prediction Engine:
  Based on a trained XGBoost classifier.  
  Returns a risk percentage (0–100%) for being diabetic.
## 3. Result Report:
  Displays prediction, advice, and risk category.  
  Includes Donut chart, descriptive risk message, and PDF download.
## 4. Report Management:
  Saves predictions into a SQLite (or similar) database.  
  Users can view, manage, and delete old reports from the dashboard.
## 5. Authentication System:
Uses Flask-Login to protect the dashboard and features.  
Shows "Sign In" or "Logout" based on login status.  
Blocks feature use unless logged in (with popups like: “Please log in to use this feature”).

# Machine Learning Part:
  Model Used: XGBoostClassifier  
  Features: 13–15 symptoms and conditions (like Polyuria, Itching, Obesity, etc.)  
  Target: Binary class — Positive or Negative for diabetes.  
  Prediction Output: Risk percentage via predict_proba.  
