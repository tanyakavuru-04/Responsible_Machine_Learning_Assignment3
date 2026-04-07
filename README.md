# Fairness Audit of Recidivism Prediction Model (COMPAS)
### Overview

This project focuses on analyzing the fairness of a recidivism prediction model built using the COMPAS dataset. The main goal is to check whether the model behaves differently across demographic groups, especially based on race and sex.

I used the model developed in the previous assignment and extended it to evaluate fairness using different statistical metrics and visualizations.

### What I Did
* Trained a classification model to predict two_year_recid
* Generated predictions on the test dataset
* Evaluated fairness across race and sex
* Performed intersectional analysis (race + sex combined)
* Compared error rates (FPR and FNR)
* Created visualizations to better understand disparities

### Fairness Metrics Used
* **Adverse Impact Ratio (AIR)** → checks if one group is disadvantaged
* **Mean Error (ME)** → difference in favorable outcomes
* **Standardized Mean Difference (SMD)** → measures magnitude of disparity
* **False Positive Rate (FPR)** → incorrect high-risk predictions
* **False Negative Rate (FNR)** → incorrect low-risk predictions

### Key Findings
* The model shows clear disparities across race
* AIR for African-American individuals is below 0.8 → indicates potential bias
* African-American individuals receive fewer favorable outcomes overall
* Differences across sex exist but are smaller

### Intersectional Insight
* African-American males are the most affected group
* They have the lowest favorable outcome rate

### Error Analysis
* African-American group → higher FPR (more false high-risk predictions)
* Caucasian group → higher FNR (more false low-risk predictions)
* Statistical tests show these differences are significant

### Visualization

A grouped bar chart was created to compare FPR and FNR across race, using Caucasian as the reference group. This helps clearly show how prediction errors differ between groups.

### Limitations
* Results depend on the model and preprocessing steps
* Fairness metrics only capture statistical differences
* Dataset may contain existing historical biases

### Conclusion

The model shows measurable fairness issues, especially across racial groups. This suggests that additional steps (like model adjustments or fairness constraints) may be needed before using it in real-world decisions.

### Tech Stack
* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib
* Solas-AI (for fairness metrics)
