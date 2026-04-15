# 🏀 NBA Salary Prediction: A Machine Learning Approach
### Predicting Player Valuation through Performance Metrics

---

## 📌 Project Overview
Can we predict an NBA player's salary based solely on their on-court performance? This project analyzes the **2020-21 season** (51 games in) to isolate "performance-driven value" from contractual noise like rookie-scale caps and veteran minimums.

## 🛠️ Tech Stack & Methodology
* **Language:** Python 3.11+
* **Libraries:** Scikit-Learn, Pandas, NumPy, Plotly (Interactive Viz)
* **Models Benchmarked:** Random Forest, Gradient Boosting, Ridge Regression

## 🧬 Data Engineering Pipeline
To ensure high **model integrity** and professional standards, I implemented the following:
* **Position Normalization:** Handled hybrid roles (e.g., `PF-C` normalized to `PF`) using string-split logic to ensure categorical consistency.
* **Leakage Prevention:** Removed "future" variables and financial indicators (e.g., `guaranteed_money`) to ensure the model relied strictly on box-score performance.
* **Feature Scaling:** Implemented a `StandardScaler` within a `Pipeline` for the Ridge model to prevent data leakage between training and test sets.

## 📊 Model Performance
I benchmarked three distinct mathematical approaches to identify the most accurate predictor:

| Model | R² Score | Mean Absolute Error (MAE) | Logic Type |
| :--- | :--- | :--- | :--- |
| **Random Forest** | **0.58** | **$3.39M** | Non-Linear / Ensemble |
| **Gradient Boosting** | 0.51 | $3.51M | Sequential Optimization |
| **Ridge Regression** | 0.35 | $4.20M | Linear w/ L2 Regularization |

## 💡 Key Insights & Feature Importance
The models consistently identified the following as the primary drivers of salary:
1.  **Age:** Highly significant due to NBA service-time rules and veteran raises.
2.  **Points (PTS):** The primary offensive volume metric.
3.  **Minutes Played (MP):** A proxy for "availability" and coaching trust.
4.  **Turnovers (TOV):** Interestingly high correlation, likely as a proxy for high usage/star players who handle the ball.

## 🚀 How to Use
1.  **Clone the Repo**
2.  **Install Dependencies:** `pip install pandas numpy plotly scikit-learn`
3.  **Run the Notebook:** Open `NBA project second draft.ipynb` to view the interactive Plotly visualizations.

---
*Created as part of the 2026 Data Analytics Portfolio.*
