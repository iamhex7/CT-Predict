# CT Predict: Identifying Low-Risk Pediatric Traumatic Brain Injury (TBI)

## Project Overview
Computed Tomography (CT) imaging for children with head injuries carries significant risks of radiation-induced malignancy. The goal of this project is to build a high-precision machine learning model to identify children at **very low risk** of Clinically-Important Traumatic Brain Injury (ciTBI). 

By accurately classifying patients for whom CT scans might be unnecessary, this model aims to assist clinical decision-making and minimize unnecessary radiation exposure in pediatric emergency departments.

## Background & Clinical Significance
This project is based on the landmark prospective observational study by **Kuppermann et al. (PECARN, 2009)**. The dataset includes clinical observations from over 30,000 pediatric patients. The primary challenge is the severe class imbalance, as ciTBI is a relatively rare but critical outcome.

## Technical Approach & Methodology

### 1. Data Engineering (R Package)
- Developed a custom R package (`hexcitbi`) to modularize the data cleaning and preprocessing pipeline.
- Handled complex clinical categorical variables and standardized features for modeling.

### 2. Modeling & Evaluation
  <img width="626" height="464" alt="image" src="https://github.com/user-attachments/assets/62c8711a-63d2-4822-9b7e-f54976c81885" /><img width="622" height="321" alt="image" src="https://github.com/user-attachments/assets/c390d6ca-58bd-4a42-9b0d-f5b70e851827" /><img width="619" height="285" alt="image" src="https://github.com/user-attachments/assets/3e29a78b-52e5-4d52-96c9-2e6d12f0e00b" />

- **Models Evaluated**: Logistic Regression (GLM), K-Nearest Neighbors (KNN), and Regularized Models (Lasso/Ridge).
- **Optimization**: Performed hyperparameter tuning using the `tidymodels` framework and cross-validation to maximize the **F1-Score**.
- **Metric Focus**: While Accuracy is high due to class imbalance, the project prioritizes **Recall (Sensitivity)** and **F1-Score** to ensure that no true ciTBI cases are missed while reducing false alarms.

### 3. Competitions
- Generated predictions on a hidden test set of 13,013 observations for a Kaggle-style competition, achieving high precision in identifying low-risk candidates.

### Technical Stack
- **Language**: R
- **Key Libraries**: `tidymodels`, `glmnet`, `kknn`, `tidyverse`, `quarto`.
- **Framework**: Developed as a structured R Package.

## Feature Importance
Clinical indicators such as **GCS (Glasgow Coma Scale) Total**, **Altered Mental Status**, and **Skull Fracture signs** were identified as the most significant predictors in the model.

## Academic Integrity & Honor Code
**Note on Code Availability:**
This project was completed as part of the **UC Berkeley STAT 133** curriculum. To uphold the **UC Berkeley Honor Code**, the source code for the R package and the final model tuning scripts is **not publicly disclosed** to prevent academic misconduct for future cohorts.

For professional inquiries or a private demonstration of the methodology (including the R package structure and cross-validation logic), please contact me at **hex@berkeley.edu**.

## Contact
- **Author**: Hex Wu
- **Email**: [hex@berkeley.edu](mailto:hex@berkeley.edu)
- **Portfolio**: [hexVerse Portfolio](https://hexverse.framer.media)
