---

# 📊 Machine Learning-Based Credit Scoring Model

## 🚀 Overview

This project assigns **credit scores** to **Aave V2 protocol wallets** using a **Gradient Boosting Regressor (GBR)** model. Scores are scaled from **0 to 1000**, quantifying wallet behavior based on historical transaction data.

---

## 📈 Score Logic

### 1️⃣ Feature Engineering

From raw transaction data, the following wallet-level features are engineered:

* **Total Transaction Count**
* **Total Transaction Volume**
* **Average Transaction Volume**
* **Number of Unique Assets Transacted**
* **Frequency of Transaction Actions:**

  * `deposit`
  * `borrow`
  * `repay`
  * `redeemunderlying`
  * `liquidationcall`

These features collectively represent wallet activity and financial behavior patterns.

---

### 2️⃣ Data Preparation

* **Scaling**: Features are standardized using `StandardScaler` to ensure uniform influence across all features during model training.

---

### 3️⃣ Model Training

* **Model Used**: `GradientBoostingRegressor` (GBR)
* **Why GBR?**
  GBR outperformed alternative models by reducing residual errors via sequential learning.

During training, the model learns relationships between wallet features and credit scores.

---

### 4️⃣ Prediction & Score Assignment

* Wallet features are passed into the trained GBR model.
* Predicted scores are **constrained to the range \[0, 1000]**, matching the designed scoring system.

---

## 🛠️ Transparency

* **Feature Importance**:
  Features like `average_volume`, `total_volume`, and `deposit frequency` contribute most significantly to predictions.

* **Model Complexity**:
  GBR, as an ensemble method, blends multiple decision trees, providing robust (though less inherently interpretable) predictions.

---

## 🔄 Extensibility

* **Feature Expansion**:
  Easily incorporate additional features (e.g., account age, inactivity periods).

* **Model Enhancements**:

  * Experiment with XGBoost, CatBoost, or ensemble multiple models.
  * Hyperparameter tuning for further optimization.

* **Re-training Pipeline**:
  New data or targets can trigger re-training with minimal pipeline changes.

---

## 📊 Conclusion

The GBR-based credit scoring model offers a **scalable** and **adaptable** solution for evaluating wallets based on transactional behavior — balancing prediction accuracy with operational transparency.

---

## 👤 Author

**Rahul Choudhary**
📧 [rahulchoudhary5266@gmail.com](mailto:rahulchoudhary5266@gmail.com)
💼 Data Science & Machine Learning Enthusiast
📬 [Connect on LinkedIn](https://www.linkedin.com/in/rahulchoudhary2000)

---
