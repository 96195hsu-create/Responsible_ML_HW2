# Responsible ML – Homework 2  
Explaining the COMPAS Replacement Model

## Files
- `L2_alignment_Jessie_Hsu.ipynb`: Full analysis and code

## Project Overview
This project analyzes a recidivism prediction model using multiple explanation methods.  
The goal is to understand how the model makes decisions and evaluate potential fairness concerns.

## Tools Used
- pandas  
- numpy  
- shap  
- lime  
- dice-ml

## How to Run
1. Open the notebook  
2. Run the cells from top to bottom  

The dataset is loaded within the notebook, so no additional setup is required.

## Methods Used
- LIME (Local explanation)
- SHAP (Global and local feature importance)
- Counterfactual analysis (DiCE)

## Workflows
### 1. SHAP Analysis
- Computed SHAP values on the test set  
- Created:
  - Beeswarm summary plot (global importance)
  - Waterfall plots for:
    - Highest-risk individual
    - Lowest-risk individual
    - Across racial groups  

### 2. LIME vs SHAP Comparison
- Applied LIME to the same individuals  
- Compared feature attributions:
  - Identified where LIME and SHAP agree  
  - Identified where they differ  
- Discussed implications of disagreement for model governance  

### 3. Counterfactual Analysis (DiCE)
- Generated counterfactuals for each individual  
- Reported minimal feature changes needed to flip predictions  
- Flagged use of immutable features (e.g., race)  

### 4. Governance Memo
- Summarized:
  - Model behavior  
  - Limitations of explanation methods  
  - Fairness concerns  
  - Recommendations for monitoring and use  

## Key Insights
- A small number of features (e.g., `priors_count`, `age`) drive most predictions  
- Explanation methods are largely consistent but differ in local detail  
- Some counterfactuals are not actionable in practice  
- Group-level disparities suggest potential fairness risks  

## Notes
This project extends the previous assignment by moving from data preparation to model explanation and evaluation.  
The focus is on interpretability, fairness, and understanding model behavior in a decision-making context.
This project is part of the Responsible Machine Learning course at GWU.
