# Stacked-Ensemble-Regression-
This project is a submission for the Child Mind Institute — Problematic Internet Use (PIU) Competition, aimed at predicting the Severity Impairment Index (SII) from a combination of physical activity (wrist-worn accelerometer data) and internet usage behavior. The dataset provided by the Child Mind Institute consists of tabular data along with time-series data, where many features contain missing values.

To build a robust predictive model, a Stacked Ensemble Regression approach is employed, combining the strengths of multiple machine learning models, including LightGBM, XGBoost, and CatBoost. This ensemble method is combined with a meta-model that integrates predictions from the base models, enhancing overall performance and capturing complex relationships in the data.

Given the challenge of missing values in the dataset, various imputation techniques were explored, with Simple Imputation being selected to replace missing data with the mean of each feature. More advanced techniques like KNN Imputation and Iterative Imputation were also considered for handling missing data in future iterations.
## Key Features of the Approach:
- Stacked Ensemble Regression: Combining three high-performing models (LightGBM, XGBoost, CatBoost) with a meta-model for enhanced prediction.
- Imputation Strategy: Missing values are handled using Simple Imputation (mean), ensuring data completeness before model training.
- Meta-Model: A Linear Regression model is used as the meta-learner, aggregating predictions from the base models to improve accuracy.
- Cross-Validation: The model performance is evaluated using cross-validation techniques to ensure generalizability and reduce overfitting.
- Quadratic Weighted Kappa (QWK): The primary evaluation metric used to assess the agreement between predicted and true SII scores, accounting for the ordinal nature of the target variable.
## Results:
The stacked ensemble model significantly improves the predictive performance on the validation set, showing promise in capturing the underlying patterns in the dataset. Future work includes exploring more sophisticated imputation techniques and hyperparameter tuning to further optimize the model’s performance.
