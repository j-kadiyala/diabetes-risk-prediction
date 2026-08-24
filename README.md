# Diabetes Risk Prediction

Predicting the likelihood of diabetes from clinical measurements using a 
Random Forest classifier, built as a portfolio project exploring machine 
learning applications in healthcare.

## Dataset

[Pima Indians Diabetes Dataset](https://raw.githubusercontent.com/jbrownlee/Datasets/master/pima-indians-diabetes.data.csv) 
— 768 patient records with 8 clinical features (glucose, BMI, blood 
pressure, age, etc.) and a binary outcome indicating diabetes diagnosis.

## Approach

- **Data cleaning:** Replaced biologically implausible zero values in 
  Glucose, BloodPressure, SkinThickness, Insulin, and BMI with the median 
  of each column, since these zeros represented missing data rather than 
  true measurements.
- **Exploratory data analysis:** Visualized feature distributions by 
  outcome and examined correlations between clinical variables.
- **Modeling:** Trained a Random Forest classifier on an 80/20 train-test 
  split to predict diabetes outcome from clinical features.
- **Evaluation:** Assessed performance on held-out test data and examined 
  feature importance to interpret model behavior.

## Results

- **Accuracy:** 74.7% on the test set
- **Top predictive features:** Glucose (26.3%), BMI (16.4%), and Age (13.5%)

These results align with established clinical knowledge — elevated blood 
glucose and higher BMI are well-known risk factors for type 2 diabetes, and 
diabetes risk is also known to increase with age.

## Limitations

This dataset is relatively small (768 patients) and drawn from a specific 
population (Pima Indian women), so the model's patterns may not generalize 
to other populations. Zero-value imputation using the median is a 
simplification — more advanced approaches (e.g. KNN or regression-based 
imputation) could improve robustness.

## Tools

Python, pandas, scikit-learn, matplotlib, seaborn — built in Google Colab.
