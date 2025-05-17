# Regression-Energy-Consumption
This project analyzes square footage needs by examining factors such as occupant numbers, temperature fluctuations, energy consumption, building types, and daily variances. Using Linear Regression, we aim to uncover insights into the relationships between these variables and spatial dimensions for accurate forecasting.

# 🔌 Energy Consumption - Linear Regression Analysis
This project is designed to explore the complexities of square footage analysis and prediction by considering a variety of influencing factors. We will examine elements such as the number of occupants, fluctuations in average temperature, patterns of energy consumption, different types of buildings, and the specific nuances of each day of the week. Our goal is to utilize Linear Regression to uncover insights that will clarify the relationships between these variables and spatial dimensions. Ultimately, we aim to enable accurate forecasting of square footage needs across diverse settings.

## 📂 Dataset

The dataset used for this analysis is:
> [Energy Consumption Dataset - Linear Regression](https://www.kaggle.com/datasets/govindaramsriram/energy-consumption-dataset-linear-regression)

Main file: `test_energy_data.csv`

## 🧪 Stages of Analysis

### 1. **Data Exploration**
- Create histograms for all features.
- Interpret distributions: multimodal, bimodal, skewed, and uniform.
- Identify numerical and categorical features.

### 2. **Pre-processing**
- Remove the target column (`Square Footage`) from the predictor features.
- Apply One-Hot Encoding to categorical features:
  - `Building Type`
  - `Day of Week`
- Merge numerical features and encoded results into `X_final`.

### 3. **Linear Regression Model**
We used two approaches:
- `LinearRegression()` from `sklearn`
- `OLS()` from `statsmodels` for comprehensive statistical interpretation.

### 4. **Model Evaluation**
- **R-squared (R²)** = 0.844 → The model explains 84.4% of the variation in square footage.
- **MSE (Mean Squared Error)** = 28,940,863 → This value is relatively low.
- Interpret coefficients to understand the influence of each feature on square footage.

### 5. **Additional Experiments**
- Conducted a simple regression using only the `Energy Consumption` feature.
- Resulting R² = 0.524 → Still indicates a strong relationship despite using just one variable.

## 📊 Main Results

| Feature | Coefficient | Interpretation |
|--------------------------|-------------|------------------------------------------------------------------------------|
| Number of Occupants | -188.22 | Adding 1 person results in a decrease of 188 sqft in square footage. |
| Average Temperature (°C) | +197.31 | An increase of 1°C leads to an increase of 197 sqft in square footage. |
| Energy Consumption | +18.01 | An increase of 1 unit in energy consumption results in an increase of 18 sqft. |
| Building Type (Industrial) | -8327.51 | Industrial buildings tend to have smaller square footage compared to the default type. |
| Building Type (Residential) | +8363.93 | Residential buildings typically have larger square footage than the default type. |
| Day of Week (Weekend) | +1228.45 | Not statistically significant (p = 0.300). |

## 🧠 Insights
- Building type and ambient temperature have a strong impact on predicting square footage.
- Energy consumption shows a positive correlation with square footage.
- The day of the week does not significantly affect square footage.

## 🛠️ Tools Used
- Python
- Pandas, Numpy
- Matplotlib
- Scikit-Learn
- Statsmodels

## 🏁 Conclusion
The regression model incorporating multiple features yields much more accurate results (R² = 0.844) compared to the simple regression using only one feature (R² = 0.524). This project highlights the importance of understanding feature context and conducting proper encoding and statistical analysis.

---

> 📌 *This project was created as part of a linear regression exercise for the Data Science & Statistics portfolio.*
