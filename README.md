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

![Final Visual Vision (Iterated Sketch 2)](https://github.com/skas901/dataviz-project-template-proposal/blob/master/iterated.png)

This sketch informs the most perceptually accurate visual encoding for the primary risk factors in the final dashboard's Small Multiples panels.

Goal: Refine the plot using VAD principles.

Position (X/Y): BMI and Glucose (High Accuracy).

Shape: Outcome (Circle for Low Risk, Cross for High Risk) (High Accuracy for Categorical).

Color Intensity: Age (Sequential Light → Dark) (Medium Accuracy for Quantitative/Ordered).


## Prototypes
![Prototype 1](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Prototype.png)

This working prototype demonstrates the use of a new technique—Arranging Tables by aggregation—which will be a key panel in the final dashboard.

Purpose: Compare the Average Glucose level between the Diabetic and Non-Diabetic groups.

## Project Progress: Implementing the Multivariate Grid
![Prototype 1](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Prototype.png)

The major progress milestone achieved is the implementation of the core visualization structure: the Multivariate Small Multiples Grid. This component uses the Arranging Tables principle to display the relationship between all major quantitative attributes simultaneously.

A. Technical Achievement: Small Multiples
The prototype now generates a matrix of scatter plots, specifically a 5x5 grid using the most predictive quantitative features: Glucose, BMI, Age, Pregnancies, and BloodPressure.

This required complex data preprocessing to transform the single patient record into an array of data points suitable for each subplot, a key step toward the final dashboard structure.

B. Visual Encoding and Analysis
Purpose: The grid allows the user to quickly scan across plots to identify which attribute pairs show the clearest separation between the diabetic and non-diabetic groups.

Position (X/Y): Varied across all subplots, representing the unique pairing of attributes (e.g., Row 3, Column 2 shows Age vs. BMI).

Color (Consistent): The Outcome (Risk) is mapped consistently to Color (e.g., Red for Diabetic, Blue for Non-Diabetic) in every single subplot. This consistency is critical for comparison.
