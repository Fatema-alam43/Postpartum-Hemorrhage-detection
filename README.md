## Postpartum Hemorrhage Machine Learning Analysis

# Overview
This repository contains a machine learning project focused on analyzing and predicting risk factors for postpartum hemorrhage (PPH), a leading cause of maternal mortality worldwide. Using clinical data from antenatal, intrapartum, and postnatal records, the Jupyter notebook Postpartum_Hemmorahge_ML.ipynb performs data preprocessing, exploratory data analysis (EDA), feature engineering, and model training to identify patterns and predict PPH outcomes.

The project leverages models such as Logistic Regression, Random Forest, and XGBoost to evaluate risk factors like maternal age, gestational age, parity, delivery method, and abnormalities (e.g., PIH, preterm labor). This work aims to support healthcare providers in low-resource settings by enabling early intervention and personalized care.

*Key Features:
- Data cleaning and categorical encoding using category_encoders.
- Visualizations with Matplotlib and Seaborn (correlation heatmaps, distribution plots).
- Model evaluation metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC.
- Inspired by studies on PPH prediction in populations like Kenya, emphasizing reproducibility and ethical data handling.

# Table of Contents

Overview
Dataset
Installation
Usage
Models and Results
Contributing
License
Acknowledgments

# Dataset
The dataset (postpartum_hemorrhage.xlsx) consists of anonymized clinical records from 223 patients, focusing on PPH cases. It includes two sheets:

RAW DATA: Original entries with 16 features, including:

Patient ID, Age (15-42 years, mean ~28), Gestational Age (GA), Booking Status (B/U), Gravida, Parity, Children Alive.
Past Obstetric Complications (e.g., previous C/S, miscarriages).
Abnormalities (e.g., PIH, Preterm Labour, Fetal Distress).
Duration of Labour, Delivery Method (NVD, LSCS, Forceps), Estimated Blood Loss (500-3000ml, mean ~900ml).
Perineum (e.g., Episiotomy, Lacerations), Birth Weight, Sex of Baby, HIV Status.


CATEGORIZED DATA: Processed version with categorized Age (1-6 scale) and Gestational Age (1-5 scale) for easier modeling.

Statistics (based on available data):

223 records (though sample shows 63 due to truncation).
PPH incidence: ~2.5% (aligned with literature).
Common Abnormalities: Nil (most), PIH, Preterm Labour, Fetal Distress.
Delivery Methods: NVD (~60%), LSCS (~38%), Forceps (~2%).

Source: Anonymized clinical data (potentially from a Kenyan cohort or similar LMIC setting). Due to medical sensitivity, ensure compliance with ethical guidelines (e.g., HIPAA/GDPR equivalents). If using for research, cite appropriately.
Note: The dataset is small; for production use, augment with larger cohorts like those from Kenya ARC (1,576 records, as in related studies).

# Installation

This project was developed using Google Colab, a cloud-based Jupyter environment with many pre-installed libraries. Below are instructions for running the notebook in Colab or locally.

1. *Open the Notebook in Colab*:
   - Upload `Postpartum_Hemmorahge_ML.ipynb` to Google Colab:
     - Go to [colab.research.google.com](https://colab.research.google.com).
     - Click **File** > **Upload Notebook** and select `Postpartum_Hemmorahge_ML.ipynb` from your local machine or GitHub.
     - Alternatively, if the notebook is in your GitHub repository, select **GitHub** in Colab and enter the URL: `https://github.com/yourusername/Postpartum-Hemorrhage-ML/blob/main/Postpartum_Hemmorahge_ML.ipynb`.

2. *Upload the Dataset*:
   - Upload `postpartum_hemorrhage.xlsx` to the Colab environment:
     - In Colab, click the Files tab (left sidebar) > Upload.
     - Select `postpartum_hemorrhage.xlsx` from your local machine.
   - Ensure the notebook’s data loading cell references the correct path (e.g., `/content/postpartum_hemorrhage.xlsx` in Colab).

3. *Install Required Libraries*:
   - Colab pre-installs `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`. Install additional libraries used in the notebook:
     !pip install category_encoders scikit-plot xgboost

