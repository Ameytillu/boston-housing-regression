## Boston Housing Regression Project

This project explores house price prediction using **Multiple Linear Regression** and **Polynomial Regression** on the classic **Boston Housing dataset**. The goal is to model the relationship between house prices and various socio-economic and housing features.

---

## Project Structure

- `BostonHousing Regression.html` – Exported HTML report of the analysis.
- `boston_housing.ipynb` – Jupyter Notebook (optional).
- Charts and visuals (e.g., heatmap, prediction plots) are embedded in the report.

---

## Dataset Overview

The dataset contains information on housing in Boston suburbs with 506 rows and 13 features. The target variable is `MEDV`, representing the **median house value in $1000s**.

### Key Features Used:
- `CRIM`: Crime rate
- `AGE`: Proportion of old buildings
- `TAX`: Property tax rate
- `RM`: Average rooms per dwelling (highly predictive)
- `LSTAT`: % lower-income residents (strong negative correlation)

---

## Exploratory Data Analysis (EDA)

- **Heatmap** reveals strong correlations of `MEDV` with `RM` (+), `LSTAT` (−), and `PTRATIO` (−).
- **Histogram of MEDV** shows a right-skewed distribution with many homes priced around $20K and a cap at $50K.
- **Boxplots** and **pairplots** were used to visualize relationships and detect outliers.

---

## Models Implemented

### 1. Multiple Linear Regression
- Simple baseline using 3 features: `CRIM`, `AGE`, and `TAX`.
- **R² Score**: ~0.26
- **RMSE**: ~7.89

### 2. Polynomial Regression (Degree 2)
- Adds squared and interaction terms.
- **R² Score**: ~0.28
- **RMSE**: ~7.79
- Slightly better fit, but still underperforms due to limited features and non-linear data structure.

---

## Performance Comparison

| Model                  | R² Score | RMSE  |
|------------------------|----------|--------|
| Linear Regression      | 0.26     | 7.89   |
| Polynomial Regression  | 0.28     | 7.79   |

The polynomial model slightly outperformed the linear model but both were limited by lack of strong features like `RM` and `LSTAT`.

---

## Evaluation Metrics

- **R² Score**: Measures how well the model explains target variability.
- **Mean Squared Error (MSE)** and **Root MSE**: Measure prediction accuracy.

---

## Insights

- Strong predictors like `RM` and `LSTAT` were not included in the baseline model, leading to lower accuracy.
- Both models underpredict high-end prices due to data cap at $50K.
- Polynomial regression slightly improved model fit for mid-range values.




