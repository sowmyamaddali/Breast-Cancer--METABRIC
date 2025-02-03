# Breast Cancer METABRIC: Survival Analysis & Predictive Modeling


## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Techniques and Tools](#techniques-and-tools)
4. [Usage](#usage)
5. [Results](#results)
6. [Future Work](#future-work)

---

## **1. Overview**
This project leverages the **Breast Cancer METABRIC dataset** to analyze survival outcomes and predict patient survival based on clinical and molecular features. The project consists of:
- **Exploratory Data Analysis (EDA)** – Understanding distributions and patterns in tumor stages, treatments, and survival times.  
- **Survival Analysis** – Applying Kaplan-Meier estimators, log-rank tests, and Cox Proportional Hazards models.  
- **Predictive Modeling** – Using **Machine Learning (Logistic Regression, Random Forest, XGBoost, Neural Networks)** to classify patients as high-risk vs. low-risk.  
- **Clustering Analysis** – Applying **K-Means clustering** to identify hidden subgroups of patients based on cancer characteristics.  

The goal is to provide **insights into survival probabilities**, the **impact of treatments and tumor characteristics**, and **hidden patient subgroups** for better risk stratification.

---

## **2. Dataset**
The [Breast Cancer METABRIC dataset](https://www.kaggle.com/datasets/gunesevitan/breast-cancer-metabric) contains data from over **2,000 breast cancer patients**, including:
- **Clinical Features**: Tumor stage, hormone therapy, chemotherapy, radiotherapy, etc.
- **Pathological Markers**: HER2 status, PR status, lymph node involvement, etc.
- **Survival Data**: Overall survival in months, relapse-free survival, patient status.

The primary goal is to **study survival time**, predict high-risk patients, and uncover potential hidden subgroups.

---

## **3. Techniques and Tools**

### **Survival Analysis**
- **Kaplan-Meier Survival Curves** – To estimate survival probabilities across tumor stages and treatment groups.
- **Log-Rank Test** – To statistically compare survival distributions.
- **Cox Proportional Hazards Model** – To assess risk factors affecting survival.

### **Predictive Modeling (Machine Learning & Deep Learning)**
- **Logistic Regression** – Baseline model for predicting patient survival.
- **Random Forest & XGBoost** – Tree-based models optimized using hyperparameter tuning.
- **Neural Networks (MLP)** – Deep learning model to improve prediction accuracy.
- **Model Performance Metrics**: **Accuracy, F1-score, ROC-AUC**.

### **Clustering Analysis (Unsupervised Learning)**
- **K-Means Clustering** – To identify hidden subgroups of patients.
- **PCA Visualization** – To reduce dimensionality and visualize clusters.
- **Cluster Interpretation** – Comparing clinical features and survival rates per cluster.

### **EDA (Exploratory Data Analysis)**
- **Distributions**:
  - Tumor Stage, Treatment (Chemo, Radio, Hormone), Age Groups
- **Correlation Analysis**:
  - Tumor Size vs Tumor Stage
  - Survival Time Across Age Groups
  - Treatment Impact on Survival
- **Boxplots & Scatter Plots** to explore **treatment outcomes** and **tumor progression trends**.

### **Tools Used**
- **Python Libraries**:  
  - `pandas`, `numpy` – Data processing  
  - `matplotlib`, `seaborn` – Visualization  
  - `lifelines` – Survival analysis  
  - `scikit-learn`, `xgboost`, `tensorflow/keras` – Machine Learning & Deep Learning  

---

## **4. Usage**
### **1. Load and preprocess the dataset**
   - **Script:** `load_preprocess_data.ipynb`
   - Cleans dataset, handles missing values, and prepares it for analysis.

### **2. Perform Exploratory Data Analysis (EDA)**
   - **Script:** `eda_analysis.ipynb`
   - Visualizes distributions, correlations, and key patterns in survival-related features.

### **3. Conduct Survival Analysis**
   - **Script:** `survival_analysis.ipynb`
   - Implements **Kaplan-Meier Curves**, **Log-Rank Tests**, and **Cox Proportional Hazards Model**.

### **4. Train Machine Learning Models for Survival Prediction**
   - **Script:** `ml_modeling.ipynb`
   - Implements **Logistic Regression, Random Forest, XGBoost, and Neural Networks**.
   - Optimizes models using **hyperparameter tuning**.
   - Evaluates model performance using **ROC-AUC and classification metrics**.

### **5. Perform Clustering Analysis**
   - **Script:** `clustering_analysis.ipynb`
   - Uses **K-Means clustering** to identify subgroups of patients.
   - Visualizes clusters with **PCA** and **analyzes survival rates per cluster**.

---

## **5. Results**
### **Predictive Modeling Insights**
- **Random Forest & XGBoost performed best (ROC-AUC: 0.79, Accuracy: 72%)**.
- **Neural Networks improved accuracy to 74% but had similar AUC (0.76)**.
- **Tumor size, Nottingham Prognostic Index, and Age were key predictive features.**

### **Clustering Analysis Insights**
- **Identified 5 patient subgroups with distinct tumor characteristics and treatment patterns.**
- **Clusters varied significantly in survival rates, confirming the existence of high-risk vs low-risk groups.**
- **Cluster 0 had the lowest survival rate, while Cluster 1 had the highest.**

### **Survival Analysis Insights**
- **Higher tumor stages correlate with lower survival probabilities.**
- **Patients with hormone therapy showed better survival outcomes.**
- **Kaplan-Meier curves showed significant survival differences across treatment groups.**

---

## **6. Future Work**
- **Enhance Predictive Modeling:**  
  - Apply **Survival Random Forests** for better survival time prediction.
  - Experiment with **Transformer-based deep learning models**.

- **Refine Clustering Approaches:**  
  - Test **Hierarchical Clustering** and **DBSCAN** for more nuanced subgroup discovery.
  - Use **SHAP analysis** to interpret clustering impact on survival.

- **Develop a Clinical Decision Tool:**  
  - Build an interactive dashboard to help doctors identify high-risk patients.
  - Incorporate clustering-based risk stratification for **personalized treatment recommendations**.

---