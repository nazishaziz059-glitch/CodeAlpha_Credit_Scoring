# CodeAlpha Credit Scoring Model

## CodeAlpha Machine Learning Internship – Task 1

### Project Overview

This project was developed as part of the **CodeAlpha Machine Learning Internship**.

The objective is to build a **Credit Scoring Model** that predicts an individual's credit risk using financial and payment-related information.

The project uses classification algorithms to classify customers into:

- **Low Risk (0)**
- **High Risk (1)**

The CodeAlpha task instructions specify classification algorithms such as **Logistic Regression, Decision Tree, and Random Forest**, with evaluation using **Accuracy, Precision, Recall, F1-Score, and ROC-AUC**.

## Objective

The main objectives are:

1. Load and understand the credit scoring dataset.
2. Clean the dataset and handle missing values.
3. Perform basic exploratory data analysis (EDA).
4. Prepare categorical data for machine learning.
5. Split the data into training and testing sets.
6. Train multiple classification models.
7. Compare model performance.
8. Select the best-performing model.
9. Test the final model on customer data.
10. Provide a simple **Gradio interface** for credit risk prediction.

## Dataset

The dataset used in this project is a **synthetic educational dataset created for this project**. It is not real bank or customer data.

It contains **5,000 records** with financial and credit-related features:

- Age
- Employment Status
- Annual Income
- Average Monthly Balance
- Number of Deposits per Month
- Debit Card Spending
- Credit Score
- Number of Open Loans
- Total Outstanding Debt
- Late Payment Count
- Previous Loan Default History
- Loan Application Amount
- Loan Repayment History
- Debt-to-Income Ratio

### Target Variable

`credit_risk`

- `0` = Low Risk
- `1` = High Risk

## Data Preprocessing

The following steps were performed:

- Checked dataset shape and information.
- Checked descriptive statistics.
- Checked missing values.
- Filled missing numerical values using the **median**.
- Filled missing categorical values using the **mode**.
- Checked for duplicate rows and removed duplicates.
- Separated features (`X`) and target (`y`).
- Encoded categorical features using **Label Encoding**.
- Split the dataset into training and testing data using an **80/20 split**.
- Used stratification to maintain the target class distribution.

## Exploratory Data Analysis

Basic EDA included:

- Credit risk class distribution
- Annual income distribution
- Credit score distribution
- Credit score comparison by risk class
- Outstanding debt comparison by risk class
- Late payment comparison by risk class
- Correlation heatmap for numerical features

## Machine Learning Models

Three classification algorithms were trained and compared:

### 1. Logistic Regression

Used as a baseline classification model.

### 2. Decision Tree

A tree-based classification algorithm that makes decisions using feature values.

### 3. Random Forest

An ensemble model consisting of multiple decision trees.

## Model Evaluation

The models were evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC**

The **F1-Score** was used as the main criterion for selecting the best model because it considers both Precision and Recall.

### Model Results


Model	Accuracy	Precision	Recall	F1-Score	ROC-AUC
0	Logistic Regression	0.722	0.617978	0.183946	0.283505	0.731917
1	Decision Tree	0.728	0.543974	0.558528	0.551155	0.679407
2	Random Forest	0.803	0.709016	0.578595	0.637201	0.844859


### Best Model

The best model is selected automatically based on the highest **F1-Score**.

The notebook also generates:

- Classification Report
- Confusion Matrix
- Random Forest Feature Importance

## Gradio Interface

A basic **Gradio interface** was created so a user can enter customer financial information and receive a credit risk prediction.

The interface accepts:

- Age
- Employment Status
- Annual Income
- Average Monthly Balance
- Deposits per Month
- Debit Card Spending
- Credit Score
- Number of Open Loans
- Total Outstanding Debt
- Late Payment Count
- Previous Loan Default
- Loan Application Amount
- Loan Repayment History

The system predicts:

**Low Risk** or **High Risk**

and displays the prediction confidence.

## Project Files

The GitHub repository contains:

```text
CodeAlpha_Credit_Scoring/
│
├── Credit_Scoring_Model_CodeAlpha.ipynb
├── CodeAlpha_Credit_Scoring_Dataset.csv
└── README.md
```

### File Description

**Credit_Scoring_Model_CodeAlpha.ipynb**  
Contains the complete Python code, preprocessing, EDA, model training, evaluation, and Gradio interface.

**CodeAlpha_Credit_Scoring_Dataset.csv**  
Contains the synthetic dataset used for training and testing.

**README.md**  
Contains the project documentation and running instructions.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Gradio
- Google Colab / Jupyter Notebook

## How to Run the Project

1. Download or clone this repository.
2. Open `Credit_Scoring_Model_CodeAlpha.ipynb` in Google Colab or Jupyter Notebook.
3. Upload `CodeAlpha_Credit_Scoring_Dataset.csv` when prompted.
4. Run the notebook cells from top to bottom.
5. The notebook will clean the data, perform EDA, train the models, compare results, select the best model, and launch the Gradio interface.

## Disclaimer

This project is created for **educational and internship purposes**.

The dataset is synthetic and the model should not be used to make real financial, banking, lending, or credit approval decisions.

## Internship Task

**Organization:** CodeAlpha  
**Task:** Machine Learning Task 1 – Credit Scoring Model  
**Project Type:** Classification / Machine Learning
