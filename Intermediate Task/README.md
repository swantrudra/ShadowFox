Loan Approval Prediction System
This repository contains a Machine Learning project that predicts whether a loan application will be approved or not based on various applicant details. The system includes data preprocessing, model training, and an interactive interface for custom predictions.

Table of Contents
Project Overview

Features

Technologies Used

Dataset

Setup and Installation

How to Run (Console Application - Google Colab)

How to Run (Streamlit UI - Google Colab)

Model Details

License

Project Overview
The goal of this project is to automate the loan eligibility process. It takes various applicant features (e.g., gender, marital status, income, loan amount, credit history) and uses a trained machine learning model to predict the Loan_Status (Approved/Not Approved).

Features
Data Preprocessing: Handles missing values (imputation), creates new features (e.g., TotalIncome, log transformations of LoanAmount and TotalIncome).

Feature Engineering: Log transformation for skewed numerical features.

Categorical Encoding: Uses LabelEncoder to convert categorical features into numerical format.

Feature Scaling: Employs StandardScaler to normalize numerical features.

Multiple ML Models: Trains and evaluates various classification algorithms:

Random Forest Classifier (used for prediction in the interactive sections)

Gaussian Naive Bayes

Decision Tree Classifier

K-Neighbors Classifier

Interactive Prediction (Console): Allows users to input custom values in the console to get a loan approval prediction.

Interactive Prediction (Streamlit UI): Provides a user-friendly web interface for inputting details and viewing predictions.

Technologies Used
Python 3.x

NumPy

Pandas

Matplotlib (for initial EDA, though not directly used in the interactive part)

Seaborn (for initial EDA, though not directly used in the interactive part)

Scikit-learn (for ML models, preprocessing, and evaluation)

Streamlit (for building the web UI)

pyngrok (for exposing Streamlit app in Google Colab)

Dataset
The project uses a dataset named loan_prediction.csv. This CSV file should contain columns relevant to loan applications, such as:

Loan_ID

Gender

Married

Dependents

Education

Self_Employed

ApplicantIncome

CoapplicantIncome

LoanAmount

Loan_Amount_Term

Credit_History

Property_Area

Loan_Status (Target variable: 'Y' for approved, 'N' for not approved)

Make sure to place loan_prediction.csv in the same directory as your Python script or upload it to your Google Colab session.

Setup and Installation
For Google Colab
Open Google Colab: Go to https://colab.research.google.com/ and create a new notebook (File > New notebook).

Upload loan_prediction.csv:

Click the "Files" icon (folder icon) on the left sidebar.

Click the "Upload to session storage" icon (file with an arrow pointing up).

Select loan_prediction.csv from your local machine and upload it.

How to Run (Console Application - Google Colab)
This version allows interaction directly within the Colab notebook's output cells.

Paste the Code: Copy the entire code block for the console application (the one that uses input() statements) into a single code cell in your Colab notebook.

(If you need this code again, ask for "Loan Approval Prediction with Console Input (for Google Colab)").

Run the Cell: Click the "Play" button next to the code cell.

Interact: The script will first train the models and print their accuracies. Then, it will prompt you for input for each applicant detail in the cell's output area. Type your response and press Enter for each prompt.

View Prediction: After all inputs are provided, the loan approval prediction will be displayed.

How to Run (Streamlit UI - Google Colab)
This version provides a web-based graphical user interface.

Install Libraries: In the first code cell of your Colab notebook, paste and run:

!pip install streamlit pyngrok

Get ngrok Authtoken:

Go to https://dashboard.ngrok.com/signup to sign up for a free ngrok account.

After logging in, go to https://dashboard.ngrok.com/get-started/your-authtoken and copy your authentication token.

Paste the Streamlit Code (with ngrok):

Create a new code cell in your Colab notebook.

Copy the entire code block for the Streamlit UI (the one that imports streamlit and includes ngrok setup at the bottom).

Crucially, find the line ngrok_auth_token = "YOUR_NGROK_AUTH_TOKEN" and replace "YOUR_NGROK_AUTH_TOKEN" with your actual ngrok token.

(If you need this code again, ask for "Loan Approval Prediction Streamlit UI").

Run the Cell: Click the "Play" button next to this code cell.

Access the UI: After a few moments, the cell output will display a public URL (e.g., https://<some_random_id>.ngrok-free.app). Click on this link to open your interactive Loan Approval Prediction UI in a new browser tab.

Model Details
The system trains and evaluates several classification models, including:

Random Forest Classifier: Often provides good accuracy and is used as the primary prediction model in the interactive interfaces.

Gaussian Naive Bayes

Decision Tree Classifier

K-Neighbors Classifier

The model performance (accuracy) on the test set is printed during the execution of the training phase.

License
This project is open-source and available under the MIT License.
