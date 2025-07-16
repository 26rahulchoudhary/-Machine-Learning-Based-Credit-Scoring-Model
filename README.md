README: Machine Learning-Based Credit Scoring Model
Overview
This project assigns credit scores to Aave V2 protocol wallets using a Gradient Boosting Regressor (GBR) model. Scores range from 0 to 1000, quantifying wallet behavior based on historical transaction data.

Score Logic
1. Feature Engineering
From raw transaction data, the following wallet-level features are engineered:

Total Transaction Count

Total Transaction Volume

Average Transaction Volume

Number of Unique Assets Transacted

Frequency of Transaction Actions:

deposit

borrow

repay

redeemunderlying

liquidationcall

These features quantify both wallet activity and financial behavior.

2. Data Preparation
Scaling: Features are standardized using StandardScaler to ensure uniform influence across all features during model training.

3. Model Training
Model Used: GradientBoostingRegressor (GBR).

Why GBR: It outperformed other models during evaluation, offering robust predictions via sequential learning and reduction of residual errors.

The model learns the mapping between wallet features and provided/predicted credit scores.

4. Prediction & Score Assignment
New wallets' features are passed to the trained GBR model.

Predicted scores are:

Constrained to [0, 1000] to align with the defined credit scoring scale.

Transparency
Feature Importance:

Features like average_volume, total_volume, and deposit frequency have the most significant influence on predictions, as derived from the GBR's built-in feature importance metric.

Model Complexity:

GBR, as an ensemble method, blends multiple decision trees.

While inherently less interpretable than simpler models, feature importance aids transparency.

Extensibility
Feature Updates: Add features (e.g., account age, wallet inactivity periods) by expanding feature engineering scripts.

Model Enhancements:

Swap in advanced models (e.g., XGBoost, CatBoost).

Perform hyperparameter tuning or ensemble multiple regressors.

Re-training:

New data or targets can trigger re-training with minimal pipeline adjustments.

Conclusion
The GBR-based credit scoring model provides a scalable and adaptable framework for evaluating wallets based on transactional behavior, balancing prediction accuracy with feature transparency.

