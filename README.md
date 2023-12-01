
# Medical Examination Data Analysis

## Overview

This project analyzes medical examination data using Python with Pandas, Seaborn, and Matplotlib. The dataset includes information such as age, gender, cholesterol levels, blood pressure, and lifestyle factors for 70,000 patients.

- **Categorical Variable Analysis**
<p align="center">
  <img width="354" alt="image" src="https://github.com/Tikii0617/Medical-Data-Visualizer/blob/master/cardio.png"> 
</p>

- **Correlation Heatmap**

  <p align="center">
  <img width="354" alt="image" src="https://github.com/Tikii0617/Medical-Data-Visualizer/blob/master/heatmap.png">
  </p>

## Project Structure

- `medical_examination.csv`: The dataset used for analysis.
- `analysis_script.py`: Python script for data analysis.

## Data Cleaning and Feature Engineering

# Load the dataset
import pandas as pd
```python
df = pd.read_csv('/Users/dejicuomu/Desktop/medical_examination.csv')
```
# Data cleaning and feature engineering
```python
df['overweight'] = (df['weight'] / (df['height'] / 100) ** 2 > 25).astype(int)
df['cholesterol'] = (df['cholesterol'] > 1).astype(int)
df['gluc'] = (df['gluc'] > 1).astype(int)
```

## Categorical Variable Analysis

```python
# Categorical variable analysis
def draw_cat_plot():
    df_cat = pd.melt(df, id_vars=['cardio'], value_vars=['cholesterol', 'gluc', 'smoke', 'alco', 'active', 'overweight'])
    df_cat['total'] = 1
    df_cat = df_cat.groupby(['cardio', 'variable', 'value'], as_index=False).count()
    df_cat.rename(columns={'total': 'total_patients'}, inplace=True)
    g = sns.catplot(x='variable', y='total_patients', hue='value', col='cardio', data=df_cat, kind='bar', ci=None, height=5, aspect=0.8)
    g.set_axis_labels('Variables', 'Total Patients')
    g.set_xticklabels(rotation=45)
    g.set_titles("{col_name} {col_var}")
    g.legend.set_title('Value')
    fig = g.fig

draw_cat_plot()
```

## Correlation Heatmap

```python
# Correlation heatmap
def draw_heat_map():
    df_heat = df[(df['ap_lo'] <= df['ap_hi']) &
                 (df['height'] >= df['height'].quantile(0.025)) &
                 (df['height'] <= df['height'].quantile(0.975)) &
                 (df['weight'] >= df['weight'].quantile(0.025)) &
                 (df['weight'] <= df['weight'].quantile(0.975))]
    corr = df_heat.corr()
    mask = np.triu(np.ones_like(corr, dtype=bool))
    fig, ax = plt.subplots(figsize=(10, 8))
    sns.heatmap(corr, mask=mask, cmap='coolwarm', vmax=.3, center=0, square=True, linewidths=.5, cbar_kws={"shrink": 0.5})
    

draw_heat_map()
```

## Results

- The analysis reveals insights into the distribution of lifestyle factors among patients and their correlation.


