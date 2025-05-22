# 🚗 Car Price Prediction
EDA

A machine learning project focused on predicting the prices of used cars based on technical specifications, performance metrics, and seller characteristics. The project combines web scraping, exploratory data analysis, and supervised regression techniques to model real-world pricing trends in the Romanian second-hand car market.

## 📌 Objectives

- Scrape comprehensive car data from [Autovit.ro](https://www.autovit.ro).
- Perform exploratory data analysis (EDA) to understand trends in pricing and car features.
- Build and compare multiple machine learning models for price prediction.
- Evaluate performance using standard regression metrics.

## 🗂️ Dataset Overview

- **Source:** [Autovit.ro](https://www.autovit.ro) (scraped using BeautifulSoup and `lxml`)
- **Total entries scraped:** ~50,000  
- **Filtered and cleaned entries:** ~20,000  
- **Features:** 61 (e.g., make, model, year, engine capacity, fuel type, emissions, etc.)
- **Target:** Car price (EUR)

### ❗ Limitations
- Prices are as listed by sellers and may include outliers or inaccuracies.
- No visual damage inspection or expert-based price correction.
- Dataset excludes electric, vintage, lease, and tuned cars for uniformity.

## 📊 Exploratory Data Analysis

The EDA phase explored:

- Price distributions
- Feature correlations
- Trends by engine power, CO₂ emissions, transmission type, and production year
- Optional feature availability by model
- Kilometers driven vs. depreciation patterns

Visualizations include heatmaps, scatter plots, bar charts, and line graphs.

## 🧪 Machine Learning Models

| Model                  | R² (Test) | MAE     | MSE        |
|------------------------|-----------|---------|------------|
| **LightGBM**           | 0.9299    | 1592.94 | 5.6M       |
| XGBoost                | 0.9251    | 1669.05 | 6.0M       |
| Gradient Boosting      | 0.9224    | 1695.48 | 6.2M       |
| Random Forest          | 0.9026    | 1840.96 | 7.8M       |
| MLP Regressor (NN)     | 0.8720    | 2192.89 | 10.3M      |
| Lasso Regression       | 0.7885    | 3067.87 | 16.9M      |

> ✅ **LightGBM Regressor** had the best performance, combining speed and accuracy with strong regularization and feature handling.

## 🛠️ Technologies Used

- Python 3
- BeautifulSoup4, lxml (Web scraping)
- Pandas, NumPy (Data manipulation)
- Matplotlib, Seaborn (Visualization)
- Scikit-learn, TensorFlow (ML)
- XGBoost, LightGBM (Advanced regressors)


## 👥 Contributors

- [Mihai Dilirici](mailto:mihai.dilirici@s.unibuc.ro)
- [Mihai-Alexandru Huțan](mailto:mihai-alexandru.hutan@s.unibuc.ro)
- [Mihai Militaru](mailto:mihai.militaru@s.unibuc.ro)
- [Marianita Cucos](mailto:marianita.cucos@s.unibuc.ro)
- [Cosmin Moarcas](mailto:cosmin.moarcas@s.unibuc.ro)

## 📜 License

Feel free to explore the code, review the findings, and contribute to improving the models

---
