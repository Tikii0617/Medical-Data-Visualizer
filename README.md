# Medical Analysis Project

## Introduction

This project involves the analysis of a medical dataset containing information about patients' health-related factors and whether they have cardiovascular diseases (cardio). The goal of this analysis is to gain insights into the relationship between various health indicators and the likelihood of having cardiovascular diseases.

## Dataset

The dataset used in this project is named `medical_examination.csv` and contains the following columns:

- `id`: Patient's ID
- `age`: Age of the patient (in years)
- `sex`: Gender of the patient (1 = male, 0 = female)
- `height`: Height of the patient (in cm)
- `weight`: Weight of the patient (in kg)
- `ap_hi`: Systolic blood pressure
- `ap_lo`: Diastolic blood pressure
- `cholesterol`: Cholesterol level (1 = normal, 2 = above normal, 3 = well above normal)
- `gluc`: Glucose level (1 = normal, 2 = above normal, 3 = well above normal)
- `smoke`: Whether the patient smokes (1 = yes, 0 = no)
- `alco`: Whether the patient consumes alcohol (1 = yes, 0 = no)
- `active`: Physical activity level (1 = active, 0 = not active)
- `cardio`: Presence of cardiovascular disease (1 = yes, 0 = no)

## Preprocessing

Before conducting the analysis, the dataset underwent preprocessing steps, including data cleaning and feature engineering. The following preprocessing steps were applied:

- Calculation of the 'overweight' feature based on BMI (Body Mass Index).
- Conversion of 'cholesterol' and 'gluc' columns into binary categorical variables.
- Handling of missing values and outliers, ensuring data quality.

## Analysis

### 1. Categorical Plot

A categorical plot was created to visualize the relationships between certain variables and the presence of cardiovascular diseases. The variables included 'cholesterol,' 'gluc,' 'smoke,' 'alco,' 'active,' and 'overweight.' This plot helps to identify any significant patterns or trends.

### 2. Heatmap

A heatmap was generated to visualize the correlation between various health-related factors. High correlation coefficients between variables can indicate relationships that may be further explored.

## Conclusion

 key findings include:

- Cholesterol and Glucose Levels Matter:
   Individuals with cardiovascular diseases tend to have higher cholesterol and glucose levels. This observation underscores the importance of managing these metabolic markers as part of preventive healthcare.

- Weight and Cardiovascular Health: Being overweight is strongly associated with an increased risk of cardiovascular diseases. Maintaining a healthy weight through diet and exercise plays a crucial role in overall heart health.

- Smoking and Cardiovascular Risk: Non-smokers are more prevalent among individuals without cardiovascular diseases. This reaffirms the well-established link between smoking and heart health, emphasizing the importance of smoking cessation programs.
- Age, Gender, and Blood Pressure: While age and gender showed correlations with cardiovascular diseases, blood pressure (systolic and diastolic) remains a significant indicator. Regular monitoring and management of blood pressure are essential for maintaining heart health.

This analysis provides valuable insights into the factors associated with cardiovascular diseases and can aid in further medical research.
