# Mortgage Prepayment Risk Prediction Using Scikit-learn Decision Tree 

This project predicts whether a mortgage will be prepaid using historical Fannie Mae loan data enriched with macroeconomic indicators. It was developed during the MIT x Break Through Tech AI Studio Challenge, under the guidance of Jonathan Zuo, AI Challenge Advisor at maka.AI. The project demonstrates an end-to-end machine learning pipeline using real-world data.

---

## 📌 Problem Statement

Mortgage prepayments can significantly impact investor returns and risk assessments. By predicting which loans are likely to be prepaid, financial institutions can make more informed decisions around asset management, refinancing, and risk modeling.

---

## 📊 Data Snapshot

**Source**: Extracted open-sourced dataset from Fannie Mae's Data Dynamics  
**File Size**: Approximately 30MB  
**Time Range**: Data spans from 2013 to 2023, with a focus on the recent period from 2017 to 2023  
**Loan Count**: A comprehensive dataset comprising around 1 million loans  
**Organization**: Data is separated by months and by different deals: G1, G2  
**Attribute Coverage**: Understanding of 108 attributes using the Data Dictionary from Data Dynamics

---

## 📁 Project Structure

mortgage-prepayment-risk/  
├── data/  # Raw and processed loan data (ignored from Git)  
├── notebooks/  # Jupyter notebooks for each pipeline stage  
├── outputs/  # Model outputs, charts, and metrics  
├── src/  # Python scripts for modular components  
├── requirements.txt  # Python dependencies  
├── .gitignore  # Files/folders to exclude from version control  
├── README.md  # Project overview and documentation  
└── LICENSE  # MIT License

---

##  Pipeline Overview

| Stage                       | Notebook                        | Description |
|----------------------------|----------------------------------|-------------|
| Data Ingestion             | `01_data_ingestion.ipynb`       | Load and clean raw Fannie Mae CRT data |
| Feature Engineering        | `02_feature_engineering.ipynb`  | Create `prepay` flag, sample cohort, explore variables |
| Macroeconomic Integration  | `03_macro_integration.ipynb`    | Merge 10-Year Treasury and Case-Shiller data |
| Model Training             | `04_model_training.ipynb`       | Apply preprocessing, train Decision Tree model |

---

##  Features

- Binary classification of loan prepayment (`prepay`)
- External data: Treasury rate (GS10), House Price Index (CSUSHPINSA)
- Custom pipeline with imputation, encoding, and state-based features
- Decision Tree Classifier using scikit-learn

---

##  How to Run

1. Clone the repository
2. Place raw CRT data and macro data into `data/raw/`
3. Open notebooks in order and run step-by-step
4. (Optional) Convert notebooks to scripts for production pipeline

---

##  Requirements

Install required packages with: see details packages needed in requirements.txt

```bash
pip install -r requirements.txt
Raw data not included due to size and licensing. 
To run this project, please download historical loan data from Fannie Mae:
https://creditrisktransfer.fanniemae.com/credit-risk-transfer/cas/historical-loan-performance

