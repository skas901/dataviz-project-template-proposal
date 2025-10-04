# Data Visualization Project

## Data

Multivariate Diabetes Risk Dashboard

This project aims to create an interactive visualization for the Pima Indians Diabetes Dataset, allowing health analysts to rapidly explore and compare multiple risk factors (BMI, Glucose, Age, Pregnancies, etc.) to understand their collective contribution to a diabetes diagnosis. This design is based on Sketch 3: The Multivariate Comparison Dashboard.

Source URL: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database

## Questions & Tasks

A. Core Questions to Answer

Prediction Threshold: Where is the precise boundary (in terms of BMI and Glucose) that separates high-risk from low-risk patients?
Risk Amplification: How does Age or Pregnancies amplify the risk when combined with high BMI and Glucose?
Factor Comparison: Which attribute (e.g., Glucose vs. BloodPressure) shows the clearest difference between the Diabetic and Non-Diabetic groups?

B. Tasks to Enable (User Goals)

Comparison: Compare the average value of any metric (e.g., Insulin) between the two categorical groups (Diabetic vs. Non-Diabetic).
Segmentation: Filter or select a specific cohort (e.g., patients with BMI > 35) and view their corresponding distributions across all other factors.
Lookup: Instantly retrieve all raw biometric data for a single patient (point) by hovering over or clicking on a mark.

## Sketches

![Final Visual Vision (Iterated Sketch 2)](https://pasteboard.co/T8La8pBfwlx0.png)

This sketch informs the most perceptually accurate visual encoding for the primary risk factors in the final dashboard's Small Multiples panels.

Goal: Refine the plot using VAD principles.

Position (X/Y): BMI and Glucose (High Accuracy).

Shape: Outcome (Circle for Low Risk, Cross for High Risk) (High Accuracy for Categorical).

Color Intensity: Age (Sequential Light → Dark) (Medium Accuracy for Quantitative/Ordered).


## Prototypes

![image](https://pasteboard.co/rPKInoSENW0w.png)

This working prototype demonstrates the use of a new technique—Arranging Tables by aggregation—which will be a key panel in the final dashboard.

Purpose: Compare the Average Glucose level between the Diabetic and Non-Diabetic groups.
