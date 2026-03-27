
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# shap-model-explainability-breast-cancer
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/shaikmahaboobsharief7/shap-model-explainability-breast-cancer.git
cd shap-model-explainability-breast-cancer 

pip install -r requirements.txt

jupyter notebook shap_explainability_tutorial.ipynb

```
----------------------------------------------------------------------------------------
# SHAP Explainability Tutorial: Interpreting Machine Learning Predictions

## Project Overview

This project demonstrates how to interpret machine learning model predictions using **SHAP (Shapley Additive Explanations)**.  

The objective is to explain:
- how individual features influence predictions  
- which features are most important globally  
- how explainability supports trustworthy AI systems  

----------------------------------------------------------------------------------------

## Dataset

The project uses the **Breast Cancer Wisconsin Diagnostic Dataset**.

- **Number of samples:** 569  
- **Number of features:** 30  
- **Target variable:** Diagnosis  
  - 1 → Malignant  
  - 0 → Benign  
----------------------------------------------------------------------------------------

## Methodology

The workflow consists of the following steps:

1. **Data Preprocessing**
   - Removed irrelevant columns (`id`, `Unnamed: 32`)
   - Encoded target variable (`M` → 1, `B` → 0)

2. **Model Training**
   - Random Forest Classifier
   - Train-test split (80/20, stratified)

3. **Model Evaluation**
   - Accuracy, classification report
   - Confusion matrix
   - ROC curve (AUC)

4. **Model Explainability using SHAP**
   - Global explanation (summary plot)
   - Feature importance (bar plot)
   - Local explanation (waterfall plot)
   - Feature behaviour (dependence plot)

----------------------------------------------------------------------------------------

## Key Results

- The model achieved **high accuracy (~97%)** on the test dataset.
- SHAP analysis revealed that features related to tumour size and shape, such as:
  - `area_worst`
  - `concave points_worst`
  - `radius_worst`  
  have the strongest influence on predictions.
- SHAP enables both **global** and **local interpretability**, improving trust in model decisions.

----------------------------------------------------------------------------------------

## Why SHAP?

SHAP is based on **Shapley values from game theory** and provides a consistent method to:

- quantify feature contributions  
- explain individual predictions  
- identify important features  
- improve transparency in machine learning  

This is especially important in domains such as healthcare, where understanding model decisions is critical.

----------------------------------------------------------------------------------------

