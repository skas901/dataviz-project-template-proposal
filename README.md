# Data Visualization Project

## Multivariate Diabetes Risk Dashboard

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

## The Sketch: Defining Visual Channels

![Final Visual Vision](https://github.com/skas901/dataviz-project-template-proposal/blob/master/sketch3.png)

The initial design focused on utilizing effective visual channels to encode multiple variables simultaneously (Multivariate Comparison Dashboard).

## Implementing the Multivariate Grid
![](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Progress.png)

The first major technical milestone was building the Small Multiples Grid. This component uses the Arranging Tables principle to display the relationship between all major quantitative attributes simultaneously.

The grid successfully generated a 5x5 matrix of scatter plots using the most predictive quantitative features. This achievement required complex data preprocessing to transform the single patient record into an array of data points suitable for each subplot, setting the stage for deep comparative analysis.

Insight: The visual consistency of mapping the Outcome to Color across every subplot was critical, allowing users to quickly scan and identify which attribute pairs showed the clearest separation between the diabetic and non-diabetic groups.

## Adding Interactivity: The Color Legend
![](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Momentum_2.png)

The implementation of the interactive color legend for Age bins added significant exploratory power. This required robust D3 state management (selectedAgeBins Set) to allow users to toggle specific age groups on and off.

Result: Users could instantly isolate specific age groups (e.g., only patients aged 60+) to analyze their BMI and Glucose levels relative to the Diabetes Outcome, fulfilling the Segmentation goal.


## The Key Upgrade: Brushing and Linking
![](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Momentum_3.png)

The integration of Brushing and Linking connected the dashboard's exploratory components. This feature allowed users to select a specific region (a "brush") on the main Scatter Plot (BMI vs. Glucose) and instantly update the summary statistics in a linked chart.


## Final Vision Realized: The 3-Panel Linked Dashboard
![](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Momentum_4.png)

The final project milestone was the full integration of all panels and interactivity features into a cohesive dashboard.

Final Dashboard Structure:

Panel 1: Multivariate Scatter Plot (BMI vs. Glucose, with Age and Outcome encoded)

Panel 2: Faceted Bar Charts (Small Multiples)

** Technique: The aggregated bar charts (Avg. Glucose by Outcome) are faceted by Age Bin.

** Impact: This panel directly addresses the Risk Amplification question, showing how the average glucose difference between the Diabetic and Non-Diabetic groups becomes most pronounced in older age cohorts.

Panel 3: Patient Detail Card

** Interactivity: Updates upon clicking a single data point in the Scatter Plot (Lookup functionality).

Key Takeaway: The seamless Brushing and Linking between Panel 1 (Scatter Plot) and Panel 2 (Faceted Bar Charts) allows analysts to select a high-risk region (e.g., high BMI/high Glucose) and immediately see the demographic breakdown of that specific cohort.

## Finishing Touches
![](https://github.com/skas901/dataviz-project-template-proposal/blob/master/Momentum_4.png)

** Visual Clarity and Completeness (Enhancements)
The code now includes key visual elements required for a professional data visualization report:

Legends Added: The renderLegends function was fully implemented to display the Age Color Legend (sequential scale) and the Outcome Shape Legend (categorical scale), explaining the multivariate encoding of the scatter plot.

Axis Units Added: All primary axes were updated with domain-specific units for clarity:

BMI: [kg/m²]

Glucose: [mg/dL]

Layout Adjusted: index.js was slightly reorganized to ensure the main plots and the new Legend Area render side-by-side, maintaining visual completeness without requiring scrolling.

## Conclusion and Live Project

The Multivariate Diabetes Risk Dashboard is a successful implementation of a multi-layered interactive visualization. It utilizes principles of effective visual encoding and advanced D3 interactivity (Brushing, Linking, Small Multiples) to provide a powerful tool for exploring multivariate risk in the Pima Indians Diabetes dataset.

Explore the final interactive dashboard here:

[https://vizhub.com/skas901/711f4be4177144b99ff76a15d866f684](https://vizhub.com/skas901/142b8a74f2544ebb8d1d3c3651833fca)
