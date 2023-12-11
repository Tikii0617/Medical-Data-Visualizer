# Medical Data Visualizer

This project involves the analysis of medical examination data to derive meaningful insights. The dataset contains information on various health-related factors for a sample of individuals. The primary objectives include visualizing categorical variables and exploring correlations between different health parameters.

## Dataset
The dataset (`medical_examination.csv`) consists of 70,000 rows and 13 columns. 
Each row represents an individual, and the columns include information such as age, sex, height, weight, blood pressure, cholesterol, glucose levels, and lifestyle factors.

## Technologies Used

- Python
- Pandas
- Seaborn
- Matplotlib
- NumPy

## Data Cleaning and Transformation

The initial exploration and preparation of the data involved:

- Checking data types and dimensions
- Creating a new 'overweight' column based on Body Mass Index (BMI)
- Transforming cholesterol and glucose columns into binary variables

## Visualization

### Categorical Variables

A categorical plot was created to visualize the distribution of patients based on various categorical variables, including cholesterol levels, glucose levels, smoking habits, alcohol consumption, physical activity, and overweight status.

<p align="center">
  <img width="354" alt="image" src="https://github.com/Tikii0617/Medical-Data-Visualizer/blob/master/cardio.png"> 
</p>

### Correlation Heatmap

A heatmap was generated to explore correlations between different health parameters. Only data within valid ranges for blood pressure, height, and weight were considered to ensure meaningful correlations.

<p align="center">
  <img width="354" alt="image" src="https://github.com/Tikii0617/Medical-Data-Visualizer/blob/master/heatmap.png">
  </p>

## Conclusion
- ### Health Indicators:
   There is a correlation between cardiovascular disease (cardio) and health indicators such as glucose (gluc) and cholesterol (chole). This suggests that individuals with higher glucose and cholesterol levels may be more prone to cardiovascular issues.

- ### Lifestyle Factors:
   Smoking behavior shows a correlation with both gender and cardiovascular disease. This implies that there might be gender-related differences in smoking habits, and smokers may have a higher likelihood of cardiovascular problems.

- ### Weight and Height:
   The correlation between weight and height indicates that taller individuals tend to weigh more on average. This is a common and expected observation.

- ### Blood Pressure and Cardiovascular Disease:
   The correlation between cardiovascular disease and diastolic blood pressure (ap_lo) suggests that individuals with specific diastolic blood pressure levels may be more susceptible to cardiovascular conditions.

- ### Age and Cardiovascular Disease:
  There is a correlation between age and cardiovascular disease, aligning with the common understanding that the risk of cardiovascular issues increases with age.

- ### Alcohol and Smoking:
   The correlation between alcohol consumption (alco) and smoking behavior implies a potential connection between these lifestyle choices. The provided Python script and visualizations offer a starting point for further analysis and exploration in the realm of health data.


