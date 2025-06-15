
## ❤️ Heart Disease Prediction using Logistic Regression

### 🧩 Overview
This project addresses the critical problem of **predicting the likelihood of a patient developing heart disease** within 10 years. Utilizing the **Framingham Heart Study dataset**, which contains various health and demographic factors, we employed **logistic regression** as a classification model. The modeling process involved initial model building and evaluation, followed by an improvement phase using **SMOTE to handle data imbalance**, resulting in a **more robust model** for predicting the minority class (heart disease).

---

### 💼 Business Understanding

Heart disease is a leading global cause of mortality. **Early detection** can save lives and reduce treatment costs.The primary stakeholders for this project would likely be healthcare professionals, medical institutions, and potentially insurance companies. The core business problem is to proactively identify individuals at high risk of developing heart disease. Early prediction allows for timely intervention, preventive measures, and personalized treatment plans, ultimately aiming to reduce the incidence and severity of heart disease, improve patient outcomes, and potentially lower healthcare costs. Research indicates that heart disease remains a leading cause of mortality globally, highlighting the significant impact of accurate prediction in healthcare strategies.

By using logistic regression, a widely used algorithm for binary classification, this project aims to:

* Predict risk of heart disease over a 10-year horizon
* Assist in preventive healthcare planning
* Support healthcare providers with data-driven decision-making

---

### 📊 Data Understanding

The data used in this analysis is the Framingham Heart Study dataset, loaded from the 'framingham.csv' file. This dataset contains various features related to patient health and lifestyle, including demographic information (e.g., age, gender), medical history (e.g., prevalent stroke, prevalent hypertension, diabetes), and health measurements (e.g., cholesterol levels, blood pressure, BMI, heart rate, glucose). The timeframe of the data is not explicitly stated in the code, but it represents a cross-section of participants from the Framingham Heart Study. Data limitations include the presence of missing values, which were handled by dropping rows with NaN values. The analysis included exploratory data visualizations such as a countplot of the target variable ('TenYearCHD') to understand class distribution.


* **Dataset**: Framingham Heart Study Dataset
* **Size**: 4,240 rows × 16 columns (after dropping missing values)
* **Target Variable**: `TenYearCHD` (binary: 0 or 1)
* **Features**:

  * Demographics: Age, Gender, Education
  * Clinical: Systolic BP, Diastolic BP, Cholesterol levels, Glucose, Heart Rate, etc.
 
    ![image](https://github.com/user-attachments/assets/9874661f-df63-4f11-8408-f867d6f51f2e)

* **Preprocessing**:

  * Handled missing values (dropped rows with NaNs)
  * Split dataset into training and testing subsets (80/20 split)

---

### 🤖 Modeling and Evaluation

* **Model Used**: A standard Logistic Regression (Binary Classification) was built and evaluated. The evaluation metrics revealed a high overall accuracy (approximately 0.83) but very poor recall (0.02) for the minority class (heart disease), indicating a strong bias towards predicting the majority class (no heart disease) due to data imbalance. The confusion matrix showed a large number of false negatives.
* **Improved Model (with SMOTE)**: To address the data imbalance, SMOTE was applied to the training data to generate synthetic samples of the minority class. A logistic regression model was then trained on this balanced dataset. The evaluation of the improved model showed a decrease in overall accuracy (approximately 0.67) but a substantial increase in recall for the minority class (0.63). The number of false negatives was significantly reduced, while the number of false positives increased. The classification report highlighted the improved recall and F1-score for the heart disease class, albeit with lower precision.

* **Why Logistic Regression**:

  * Interpretable coefficients
  * Suitable for medical risk estimation
* **Evaluation Metric**:

  * Accuracy Score
  * Recall
  * Classification Report
  * Confusion Matrix
* **Performance**:

  * The original model was optimized for overall correct predictions, while the improved model was optimized for identifying the positive class, a more relevant goal in a medical context.
* **Top 10 Performing Features**:We get the coefficients of the trained logistic regression model using model_improved.coef_[0]. The coefficients represent the weight assigned to each feature in the model. A higher absolute coefficient value indicates a stronger influence on the prediction.
  ![image](https://github.com/user-attachments/assets/a1c017ba-da8d-4a94-98d6-57bb02e925c6)

---

### 📌 Conclusion
The **improved logistic regression model, trained on SMOTE-resampled data**, demonstrates a significant improvement in identifying individuals at risk of heart disease compared to the initial model. While the overall accuracy is lower, the increased recall for the heart disease class is crucial for proactive healthcare interventions.

* Logistic Regression effectively predicted the 10-year heart disease risk
* Model could serve as an assistive tool in health screening programs
* Future scope includes comparing with advanced models like Random Forest or XGBoost for better performance

---

