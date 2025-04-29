# Evaluation: What Drives Used Car Prices?
## Business Objective Recap
- Client: Used car dealership.
- Objective: Identify what factors drive vehicle pricing to better advise sellers/buyers and optimize inventory pricing.
- Technical Goal: Build robust predictive models to explain price variations.

## Modeling Summary
- Exploratory Data Analysis (EDA): Important relationships — e.g., condition, odometer, year, manufacturer were visualized.
- Feature Engineering:
  - Label encoding and scaling performed.
  - Polynomial features is an opportunity, that can possibly be leveraged.
- Modeling Approaches:
  - Linear Regression (Baseline)
  - Lasso Regression (L1 Regularization)
  - Ridge Regression (L2 Regularization)
  - GridSearchCV and KFold cross-validation for hyperparameter tuning.
  - Finally XGBoost was leveraged as exploratory regressor for improving model performance
- Evaluation Metric: R² Score.
- Current Best Model Performance:
  - R² ~ 0.65–0.66 (For regressor models like MultiLinear, Ridge, and Lasso regressors leaving decent but room to improve).
  - R² ~ 0.87 - 0.89 for XGBoost regressor.

## Key Insights from Data
- Odometer: Strong negative correlation with price.
- Vehicle Year: Newer models command higher prices.
- Condition: Major driver; 'Excellent' and 'Like New' vehicles are priced significantly higher.
- Manufacturer Effects: Certain brands (e.g., Lexus, BMW, Toyota) have premium pricing.
- Type/Body Style: SUVs, trucks tend to be higher priced than sedans or hatchbacks.

## Improvements
1. **Outlier Handling**:
        - Price outliers (e.g., luxury sports cars) still influence the model.
        - Use robust scaling techniques or remove extreme values.
2. **Feature Expansion**:
        - Using Polynomial terms.
3. **Categorical Encoding**:
        - Explore other categorical encoders for improved results.

## Client recommedation:
Key price drivers include vehicle age, mileage, manufacturer, and condition. 
  - Newer vehicles or vehicles with low odometer reading has better price value. 
  - Certain makes retain value much better. 
  - Condition of the vehicle has significant impact on the price. 
  - Title status has a massive impact. Salvage titles can reduce the price significantly. 
  - Diesel engines and truck retain value better than economy models. 

**For even better accuracy, additional richer feature set like vehicle history for feature engineering could be leveraged**. 
