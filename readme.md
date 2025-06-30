# 🛒 On-Time Delivery Prediction – Logistic Shipping Dataset

## 📌 Project Overview

This project aims to build a classification model capable of predicting whether a delivery will arrive on time or not, based on shipping, logistics, and customer service data from an e-commerce company.

The project covers all stages of a data science workflow, including data exploration, feature engineering, outlier detection, model training, and evaluation.

---

## 📊 Dataset Description

The dataset contains 11,000+ records with the following key features:

- `Warehouse_block` – Warehouse identifier (categorical)
- `Mode_of_Shipment` – Transportation mode
- `Customer_care_calls` – Number of customer service calls
- `Customer_rating` – Rating given by the customer (1 to 5)
- `Cost_of_the_Product`, `Discount_offered`, `Weight_in_gms`
- Target: `Reached.on.Time_Y.N` (1 = on time, 0 = late)

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights:
- Heavily discounted and heavier shipments were more likely to arrive late.
- Road shipment was the most frequent and also had higher delay rates.
- Distribution of the target variable was slightly imbalanced (approx. 60/40).

Visualizations:
- Histograms, boxplots, correlation heatmaps, pairplots
- Class-wise distribution for key features

---

## 🧼 Data Preprocessing

Steps performed:
- Dropped irrelevant columns (`ID`)
- Renamed target column to `on_time`
- Applied **Label Encoding** to categorical features
- Scaled features using **StandardScaler**
- Detected outliers with **Local Outlier Factor (LOF)**
- Calculated **VIF** to reduce multicollinearity
- Created new features:
  - `cost_per_weight`, `discount_per_cost`, `calls_per_weight`, `purchase_per_weight`

---

## 🤖 Modeling

The following models were trained and evaluated:
- Naive Bayes
- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Random Forest
- Support Vector Machine
- Neural Network (MLPClassifier)

### ✅ Evaluation Metrics:
- Accuracy
- Precision / Recall / F1-Score
- R² Score
- Cross-validation (30 iterations) with mean and std deviation

The **Neural Network model** achieved the best results:
- **Accuracy**: ~86%
- **F1-Score**: 0.86
- **Stable cross-validation metrics**

---

## 💡 Conclusions

The model is capable of identifying late deliveries with high accuracy, offering logistics teams a chance to act preventively.

**Potential business applications:**
- Prioritizing critical shipments
- Resource allocation to reduce delays
- Improving customer satisfaction

---

## 📈 Future Improvements

- Add external variables (e.g., distance, weather, holidays)
- Test ensemble methods like XGBoost or LightGBM
- Deploy the best model using Flask or Streamlit
- Automate pipeline with Apache Airflow or Prefect

---

## 🚀 Tech Stack

- Python (Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn)
- Jupyter Notebook
- LOF, VIF, StandardScaler, GridSearchCV
- Git, Joblib

---

## 🗂️ Files

- `__init__.ipynb`: Full source code (notebook format)
- `__init__.pdf`: Printable version of the analysis
- `shipment.csv`: Source dataset

---

## 📬 Author

**Thales Santos Ferreira**  
Consultant | RPA Developer | Data Science Student  
[LinkedIn](https://www.linkedin.com/in/thales-sf/) • [GitHub](https://github.com/seuusuario)