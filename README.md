# Car Price Prediction Using XGBoost

This project aims to predict the price of used cars using machine learning techniques, specifically leveraging the power of the XGBoost algorithm. The model is trained on various car attributes such as mileage, engine size, age, and transmission type, with the goal of maximizing accuracy (R² score) while keeping the model fast and interpretable.

---

## 🔍 Project Overview

- **Problem**: Predict the selling price of a used car based on its features.
- **Approach**: Use cleaned and feature-engineered data with an XGBoost regression model.
- **Goal**: Achieve a high R² score with minimal overfitting.
- **Final Model R²**: **0.8191**

---

## 📂 Dataset

- Source: `Car_Price_Prediction.csv`
- Features used:
  - `Mileage` — total distance driven
  - `Engine Size` — in liters
  - `Car_Age` — current year (2025) minus year of manufacture
  - `Transmission_Manual` — 1 if manual, 0 if automatic

Additional engineered features:
- `Mileage_per_Year`  
- `Engine_per_Year`  
- Outliers were capped and some features dropped based on importance.

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **XGBoost 3.0.3**
- **scikit-learn**
- **pandas**
- **NumPy**
- **Matplotlib / Plotly** (for visualization)
- **Jupyter Notebook / PyCharm IDE**

---

## 🚀 Model Training & Tuning

- Used `GridSearchCV` for hyperparameter optimization
- Trained on GPU using:
  ```python
  params = {
      'max_depth': 4,
      'learning_rate': 0.01,
      'n_estimators': 500,
      'subsample': 0.8,
      'colsample_bytree': 0.7,
      'tree_method': 'hist',
      'device': 'cuda',
      'objective': 'reg:squarederror'
  }
````

---

## 📈 Results

| Metric      | Score            |
| ----------- | ---------------- |
| R² Score    | 0.8191           |
| RMSE (test) | *Varies per run* |
| MAE (test)  | *Varies per run* |

---

## 🧠 Future Improvements

* Deploy as a web app using Streamlit
* Add more domain-specific features (e.g., service history, accident reports)
* Introduce explainability using SHAP values
* Build an API for car dealerships to plug in real-time data

---

## 🤝 Credits

* Developed by [Pranshu Singh]([https://github.com/pranshusingh0](https://github.com/PranshuXI))
* Guidance & tuning support via \[ChatGPT + personal research]

```

---

Let me know if you want:
- A `requirements.txt`
- A `train.py` script from your notebook
- A **Streamlit UI template**

All of this can be bundled for a solid portfolio repo in under an hour. Want to go for it?
```
