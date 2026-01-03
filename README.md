# Titanic Survival Prediction Using Logistic Regression

## Executive Summary
This project applies a supervised machine learning approach to predict passenger survival on the Titanic using demographic and ticket-related attributes. A logistic regression model is trained on historical passenger data to identify which factors most strongly influenced survival outcomes. The model achieves solid predictive performance and demonstrates how structured data preprocessing and interpretable classification models can be used to solve real-world binary prediction problems.

---

## Business Problem
In high-risk environments, decision-making often depends on limited and imperfect information. Understanding which characteristics are associated with survival outcomes can help inform risk assessment, prioritization, and resource allocation.

While the Titanic dataset is historical, the analytical problem mirrors modern use cases such as:
- Risk scoring
- Survival or default prediction
- Binary classification under uncertainty

This project addresses the question:
**Which passenger attributes most strongly predict survival, and how accurately can survival be predicted using a simple, interpretable model?**

---

## Data Overview
The analysis uses the well-known Titanic passenger dataset, which contains demographic and travel information for individuals aboard the ship.

**Key features include:**
- Passenger class
- Sex
- Age
- Number of siblings/spouses aboard
- Number of parents/children aboard
- Fare paid
- Port of embarkation

The target variable is **Survived**, indicating whether a passenger lived or died.

---

## Methodology
- Performed data quality checks and handled missing values
  - Dropped high-missingness features
  - Imputed missing ages using the mean
  - Filled missing embarkation values using the mode
- Converted categorical variables into numeric form for model compatibility
- Removed identifier and text fields not suitable for prediction
- Split data into training (80%) and testing (20%) sets
- Trained a logistic regression classifier
- Evaluated model performance using accuracy on training and test data
- Implemented prediction logic for new, unseen passenger profiles

The approach prioritizes interpretability and reproducibility over model complexity.

---

## Skills Demonstrated
**Technical Skills**
- Data cleaning and preprocessing in Python
- Handling missing data and feature transformation
- Binary classification using logistic regression
- Train-test splitting and model evaluation
- Predictive modeling with scikit-learn

**Analytical & Business Skills**
- Framing a prediction problem from raw data
- Interpreting model outputs in a real-world context
- Balancing model simplicity and performance
- Communicating results to non-technical audiences

---

## Results
- The logistic regression model achieved:
  - ~81% accuracy on training data
  - ~78% accuracy on test data
- Performance indicates reasonable generalization with limited overfitting
- Gender, passenger class, and fare emerged as influential predictors
- The model successfully generates survival predictions for hypothetical passengers

These results demonstrate that even simple models can provide meaningful insights when paired with thoughtful data preparation.

---

## Interpretation
Passenger survival was not random. Structural and demographic factors played a significant role in outcomes, reflecting real-world constraints such as access to lifeboats and evacuation prioritization. Logistic regression offers a transparent way to quantify these relationships while maintaining predictive usefulness.

---

## Limitations
- Model performance is constrained by limited feature richness
- Nonlinear relationships and interactions are not explicitly modeled
- Accuracy alone does not capture all aspects of classification quality
- Historical context limits direct generalization to modern settings

---

## Business Implications
- Simple, interpretable models can be effective for high-stakes binary decisions
- Feature quality and preprocessing matter as much as model choice
- Logistic regression remains a strong baseline for risk and survival modeling
- This workflow is applicable to domains such as credit risk, fraud detection, and operational triage

---

## Next Steps
- Evaluate additional metrics such as precision, recall, and ROC-AUC
- Explore feature interactions or nonlinear models
- Perform hyperparameter tuning and cross-validation
- Compare results with alternative classification algorithms

---

## Repository Contents
- `/scripts`: Python script for data preprocessing, modeling, and prediction
- `/data`: Training and test datasets used for model development
