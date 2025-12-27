***Airbnb Price Determinants in Milan***
**Project Overview**

This project analyzes the key factors affecting Airbnb listing prices in Milan using a combination of classical econometric models and machine learning techniques. The primary objective is to understand which listing characteristics drive prices and to evaluate whether more complex models provide meaningful performance improvements over interpretable linear approaches.

Rather than focusing solely on predictive accuracy, the project emphasizes data quality, feature engineering, model diagnostics, and out-of-sample validation.

**Data Description**

The dataset contains Airbnb listings in Milan and includes information on:

Capacity-related features (accommodates, bedrooms, bathrooms, beds)

Room type

Location and review scores

Amenities (WiFi, TV)

Listing price

Due to strong right skewness in prices, the target variable is modeled using a logarithmic transformation.

**Methodology**

The analysis follows these steps:

*Exploratory Data Analysis (EDA)*

Examination of price distribution

Log transformation of the target variable

Price differences across room types

*Data Preprocessing*

Median imputation for missing numerical values

Encoding of categorical variables

Feature selection based on interpretability and availability

*Modeling*

Ordinary Least Squares (OLS) regression as a baseline

Lasso regression for feature selection and coefficient stability

XGBoost as a non-linear benchmark model

*Model Validation*

Train/test split

Evaluation using MAE, RMSE, and R² metrics

**Results**

OLS regression explains approximately 28–39% of price variance, depending on feature set

Capacity-related variables and room type are the strongest predictors

Lasso confirms redundancy among several correlated features

XGBoost does not significantly outperform linear models given limited feature richness

These results suggest that increased model complexity does not automatically lead to better performance when explanatory variables are constrained.

**Key Takeaways**

Log transformation is essential for stabilizing variance in Airbnb price data

Interpretability and data quality often outweigh algorithmic complexity

Linear models remain competitive benchmarks for structured tabular data

Feature availability is a major bottleneck for predictive performance

*Technologies Used*

Python

pandas, numpy

matplotlib, seaborn

scikit-learn

statsmodels

XGBoost
