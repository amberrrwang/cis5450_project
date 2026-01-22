# Steam Applications Price Prediction

## Project Overview

This is a data science and analytics project that uses historical Steam application data to build and evaluate machine learning models that predict app prices.  
This project aims to explore data preprocessing, feature engineering, model training and evaluation. The project was completed as part of the CIS 5450 (Big Data Analytics) course at the University of Pennsylvania. 

---

## Data Source

The dataset is derived from publicly available Steam application metadata, containing records and over 70 features per game. Key variables include:

- Pricing information (initial price, discounts)
- Game attributes (genres, categories, release date)
- User engagement metrics (reviews, playtime statistics)
- Platform and language support
- Developer and publisher information

Extensive preprocessing was required to address missing values, high-cardinality categorical variables, skewed distributions and outliers commonly observed in game pricing data.

---

## Methods

The project follows a standard machine learning workflow:

### Data Cleaning & Preprocessing
- Removed invalid, duplicate and missing entries
- Dropped unrelated or low-information features (e.g., identifiers, URLs, text fields not used for modeling)
- Encoded categorical variables and scaled numerical features
- Explored dimensionality reduction using PCA

### Exploratory Data Analysis (EDA)
- Examined price distributions and long-tail behavior
- Analyzed correlations between pricing, reviews, and playtime
- Identified outliers and nonlinear relationships

### Modeling
- Trained and evaluated multiple regression models, including:
  - Random Forest
  - CatBoost / XGBoost
- Conducted hyperparameter tuning
- Compared PCA vs non-PCA feature representations

### Evaluation
- Assessed model performance using RMSE and R²
- Evaluated generalization using validation data
- Interpreted feature importance to identify key price drivers

---

## Key Findings

- Tree-based ensemble models (e.g., Random Forest and CatBoost) significantly outperformed linear baselines, capturing nonlinear pricing dynamics
- User engagement metrics, game genres, and platform/language support were among the most influential features for predicting price
- Dimensionality reduction via PCA did not consistently improve performance, indicating that preserving original feature structure is beneficial for tree-based models
- Overall, the results suggest that Steam game pricing is driven by both content characteristics and expected market reach

