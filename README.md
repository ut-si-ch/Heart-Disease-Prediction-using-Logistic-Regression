
## ❤️ Heart Disease Prediction using Logistic Regression

### 🧩 Overview

This project leverages **logistic regression** to predict the likelihood of a person developing heart disease within 10 years, using clinical and demographic data. It demonstrates how machine learning can be applied to make meaningful predictions in healthcare for early intervention.

---

### 💼 Business Understanding

Heart disease is a leading global cause of mortality. **Early detection** can save lives and reduce treatment costs. By using logistic regression, a widely used algorithm for binary classification, this project aims to:

* Predict risk of heart disease over a 10-year horizon
* Assist in preventive healthcare planning
* Support healthcare providers with data-driven decision-making

---

### 📊 Data Understanding

* **Dataset**: Framingham Heart Study Dataset
* **Size**: 4,240 rows × 16 columns (after dropping missing values)
* **Target Variable**: `TenYearCHD` (binary: 0 or 1)
* **Features**:

  * Demographics: Age, Gender, Education
  * Clinical: Systolic BP, Diastolic BP, Cholesterol levels, Glucose, Heart Rate, etc.
* **Preprocessing**:

  * Handled missing values (dropped rows with NaNs)
  * Split dataset into training and testing subsets (80/20 split)

---

### 🤖 Modeling and Evaluation

* **Model Used**: Logistic Regression (Binary Classification)
* **Why Logistic Regression**:

  * Interpretable coefficients
  * Suitable for medical risk estimation
* **Evaluation Metric**:

  * Accuracy Score
* **Performance**:

  * Achieved strong predictive power (specific accuracy score can be included if available)

---

### 📌 Conclusion

* Logistic Regression effectively predicted the 10-year heart disease risk
* Model could serve as an assistive tool in health screening programs
* Future scope includes comparing with advanced models like Random Forest or XGBoost for better performance

---

