
# Loan Approval Prediction System

This repository contains a Machine Learning project that predicts whether a loan application will be approved or not based on various applicant details. The system includes data preprocessing, model training, and an interactive interface for custom predictions.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Setup and Installation](#setup-and-installation)
- [How to Run (Console Application - Google Colab)](#how-to-run-console-application---google-colab)
- [How to Run (Streamlit UI - Google Colab)](#how-to-run-streamlit-ui---google-colab)
- [Model Details](#model-details)
- [License](#license)

## Project Overview
The goal of this project is to automate the loan eligibility process. It takes various applicant features (e.g., gender, marital status, income, loan amount, credit history) and uses a trained machine learning model to predict the Loan_Status (Approved/Not Approved).

## Features
- **Data Preprocessing**: Handles missing values (imputation), creates new features (e.g., TotalIncome, log transformations of LoanAmount and TotalIncome).
- **Feature Engineering**: Log transformation for skewed numerical features.
- **Categorical Encoding**: Uses LabelEncoder to convert categorical features into numerical format.
- **Feature Scaling**: Employs StandardScaler to normalize numerical features.
- **Multiple ML Models**:
  - Random Forest Classifier (used for prediction in the interactive sections)
  - Gaussian Naive Bayes
  - Decision Tree Classifier
  - K-Neighbors Classifier
- **Interactive Prediction (Console)**: Allows users to input custom values in the console to get a loan approval prediction.
- **Interactive Prediction (Streamlit UI)**: Provides a user-friendly web interface for inputting details and viewing predictions.

## Technologies Used
- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Streamlit
- pyngrok

## Dataset
The project uses a dataset named `loan_prediction.csv`. This CSV file should contain columns relevant to loan applications, such as:

- Loan_ID
- Gender
- Married
- Dependents
- Education
- Self_Employed
- ApplicantIncome
- CoapplicantIncome
- LoanAmount
- Loan_Amount_Term
- Credit_History
- Property_Area
- Loan_Status

Make sure to place `loan_prediction.csv` in the same directory as your Python script or upload it to your Google Colab session.

## Setup and Installation

### For Google Colab
1. **Open Google Colab**: https://colab.research.google.com/
2. **Upload Dataset**: Upload `loan_prediction.csv` to your session storage.

## How to Run (Console Application - Google Colab)
1. Paste the code with `input()` prompts into a code cell in Colab.
2. Run the cell.
3. Input values when prompted.
4. View the loan approval prediction output.

## How to Run (Streamlit UI - Google Colab)
1. Install libraries:

    ```bash
    !pip install streamlit pyngrok
    ```

2. Get your ngrok auth token from: https://dashboard.ngrok.com/get-started/your-authtoken
3. Paste Streamlit + ngrok setup code in a new Colab cell.
4. Replace `"YOUR_NGROK_AUTH_TOKEN"` with your actual token.
5. Run the cell and click the generated ngrok URL to access the web UI.

## Model Details
Models used:
- Random Forest Classifier (default)
- Gaussian Naive Bayes
- Decision Tree Classifier
- K-Neighbors Classifier

Model accuracies are printed during training.

## License
This project is open-source and available under the MIT License.
