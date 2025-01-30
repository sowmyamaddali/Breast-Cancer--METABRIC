# Survival Analysis on Breast Cancer METABRIC Dataset


## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Techniques and Tools](#techniques-and-tools)
4. [Usage](#usage)
5. [Results](#results)
6. [Future Work](#future-work)

---

## **1. Overview**
This project leverages the **Breast Cancer METABRIC dataset** to analyze survival outcomes, focusing on identifying **clinical and molecular factors** influencing patient survival.  
Key analyses include:
- **Exploratory Data Analysis (EDA)** – Understanding distributions and patterns in tumor stages, treatments, and survival times.  
- **Survival Analysis** – Applying Kaplan-Meier estimators, log-rank tests, and Cox Proportional Hazards models.  
- **Data Imputation & Preprocessing** – Handling missing values using mode imputation.  

The goal is to provide **insights into survival probabilities** and the **impact of treatments, tumor characteristics, and patient demographics**.

---

## **2. Dataset**
The [Breast Cancer METABRIC dataset](https://www.kaggle.com/datasets/gunesevitan/breast-cancer-metabric) contains data from over **2,000 breast cancer patients**, including:
- **Clinical Features**: Tumor stage, hormone therapy, chemotherapy, radiotherapy, etc.
- **Pathological Markers**: HER2 status, PR status, lymph node involvement, etc.
- **Survival Data**: Overall survival in months, relapse-free survival, patient status.

The primary goal is to **study survival time** and its influencing factors.

---

## **3. Techniques and Tools**
### **Survival Analysis**
- **Kaplan-Meier Survival Curves** – To estimate survival probabilities across tumor stages and treatment groups.
- **Log-Rank Test** – To statistically compare survival distributions.
- **Cox Proportional Hazards Model** – To assess risk factors affecting survival.

### **EDA (Exploratory Data Analysis)**
- **Distributions**:
  - Tumor Stage, Treatment (Chemo, Radio, Hormone), Age Groups
- **Correlation Analysis**:
  - Tumor Size vs Tumor Stage
  - Survival Time Across Age Groups
  - Treatment Impact on Survival
- **Cluster Analysis**:
  - Patients where **Relapse-Free Status ≈ Overall Survival**
  - **Stage 3 vs Stage 4 survival patterns**
- **Boxplots & Scatter Plots** to explore **treatment outcomes** and **tumor progression trends**.

### **Data Imputation**
- **Mode Imputation** – Used for handling missing categorical values.

### **Tools Used**
- **Python Libraries**:  
  - `pandas`, `numpy` – Data processing  
  - `matplotlib`, `seaborn` – Visualization  
  - `lifelines` – Survival analysis  

---

## **4. Usage**
### **1. Load and preprocess the dataset**
   - **Script:** `load_preprocess_data.ipynb`
   - Cleans dataset, performs **mode imputation**, and prepares it for analysis.

### **2. Perform Exploratory Data Analysis (EDA)**
   - **Script:** `eda_analysis.ipynb`
   - Visualizes distributions, correlations, and key patterns in survival-related features.

### **3. Conduct Survival Analysis**
   - **Script:** `survival_analysis.ipynb`
   - Implements **Kaplan-Meier Curves**, **Log-Rank Tests**, and **Cox Proportional Hazards Model**.

---

## **5. Results**
### **Key Findings from EDA**
**Stage 2 is the most common tumor stage (~1700 cases).**  
**Survival probability decreases with increasing age.**  
**Patients with hormone therapy tend to have longer survival times.**  
**Chemotherapy is selectively applied, mostly in aggressive cases.**  
**Kaplan-Meier analysis confirms lower survival probabilities for Stage 3 & 4 patients.**  

### **Survival Analysis Insights**
**Higher tumor stages correlate with lower survival probabilities.**  
**Patients with relapse-free survival ≈ overall survival represent a key subgroup for analysis.**  
**Kaplan-Meier curves show significant survival differences across treatment groups.**  
**Cox Proportional Hazards Model will be applied next to quantify risk factors.**  

---

## **6. Future Work**
- **Expand Survival Modeling**
  - Apply **Cox Proportional Hazards Model** to estimate the influence of multiple factors on survival time.
  - Investigate **non-linear survival models** (e.g., Random Survival Forests).
  
- **Optimize Treatment Analysis**
  - Assess the impact of **treatment combinations** on survival rates.
  - Compare survival trends in patients receiving **single vs. multiple treatments**.

- **Develop a Predictive Model**
  - Build a **risk stratification tool** for predicting **high-risk patients**.
  - Use machine learning approaches for **advanced survival prediction**.

---

