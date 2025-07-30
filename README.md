# Predictive Modeling of Startup Success

Developed an end-to-end machine learning pipeline to rigorously test the viability of predicting startup success from a public dataset. This project involved advanced data cleansing, feature engineering, and the systematic evaluation of a Random Forest regression model using Python and Scikit-learn, all within AI4ALL's cutting-edge **AI4ALL Ignite** accelerator. Our primary finding was a critical analysis of the dataset's integrity, demonstrating a mature, scientific approach to data validation.

---

## Problem Statement

Given the recent surge in new business ventures and the historically high failure rate of startups, entrepreneurs lack reliable, data-driven tools to assess their potential for success. This project was motivated by the need to move beyond anecdotal evidence and create a model that could identify the key drivers of success, providing actionable insights to founders in the critical early stages of their companies.

---

## Key Results

- **Initial Data Validation Failure**  
  Our initial analysis on a global startup dataset revealed a critical flaw. After training multiple models, we consistently received negative R-squared values, leading us to conclude that the provided Success Score was statistically random and not correlated with the features.

- **Project Pivot and Metric Engineering**  
  We pivoted to a new, more reliable dataset, which presented a new challenge: it lacked a success metric. We engineered a new, defensible **Success Score** based on clear outcome variables (like IPO status, acquisition, and valuation), allowing us to build a meaningful model while avoiding data leakage.

- **Successful Model Development**  
  Using the new dataset and our engineered success metric, we successfully trained a **Random Forest Regressor**. The final model achieved a positive R-squared score of **0.6826**, demonstrating a moderately strong predictive relationship between a startup's characteristics and its potential for success.

- **Output Transformation for User Experience**  
  We observed that the model's raw predictions were clustered in a narrow range (1.0 to 1.5). To provide a more intuitive output for the end-user, we implemented a final transformation to scale the raw score to a clear **0–1 range**, where 0 represents lower potential and 1 represents higher potential.

---

## Methodologies

- Extensive data preparation pipeline using **Pandas**:
  - One-hot encoding categorical variables
  - Engineering features like *Startup Age* and *financial efficiency ratios*
  - Log-transformations to handle heavily skewed data
  - Outlier detection using **Interquartile Range (IQR)** method

- Modeling with **Scikit-learn**:
  - Trained a `RandomForestRegressor`
  - Used **5-fold cross-validation** for robust evaluation

---

## Data Sources

- **Kaggle Dataset**: [Startup Investments Crunchbase](https://www.kaggle.com/datasets/arindam235/startup-investments-crunchbase)

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib & Seaborn  
- Plotly Express  

---

## Authors

This project was completed in collaboration with:

- Ebyan Jama  
- Sarah Toussaint  
- Shirina Shaji Daniel  
- **Victor Olivo**  
- Elisa Yu
