# 🚗 Vehicle Price Prediction — Machine Learning Project

This project builds a predictive model to estimate used vehicle prices based on a cleaned Craigslist dataset.  
It includes full preprocessing, model training, evaluation, and interpretation.

---

## 📊 1. Project Overview

The goal of this project is to understand which factors most influence vehicle prices and to build a model capable of predicting price from listing features such as year, mileage, condition, manufacturer, and body type.

---

## 🧹 2. Data Cleaning & Preprocessing

- Removed duplicates and irrelevant columns  
- Handled missing values  
- Encoded categorical variables  
  - One‑hot encoding for baseline models  
  - Native categorical handling for CatBoost  
- Scaled numerical features  
- Split data into training and testing sets  

---

## 🤖 3. Models Trained

### **Linear Regression**
- Simple, interpretable baseline  
- Performs reasonably well on linear relationships  

### **Random Forest Regressor**
- Nonlinear ensemble model  
- Struggles with high‑cardinality categorical features  

### **CatBoost Regressor**
- Gradient boosting model designed for tabular data  
- Handles categorical variables natively  
- Achieved the best performance by a wide margin  

---

## 📈 4. Model Performance

| Model              | MAE     | RMSE    | R²     |
|-------------------|---------|---------|--------|
| Linear Regression  | 6036    | 8831    | 0.633  |
| Random Forest      | 10964   | 14036   | 0.074  |
| **CatBoost**       | **807** | **1777** | **0.985** |

CatBoost dramatically outperformed all other models, achieving an R² of 0.985 and the lowest error metrics.  
Its ability to process categorical features without one‑hot encoding makes it ideal for this dataset.

---

## 🔍 5. Key Insights

- Newer vehicles and lower mileage strongly increase price  
- Condition and manufacturer are major value drivers  
- Trucks, SUVs, and AWD/4WD vehicles tend to be priced higher  
- CatBoost reveals complex interactions that simpler models miss  
- High‑cardinality categorical features require models that handle them natively  

---

## 📝 6. Conclusion

CatBoost proved to be the most effective model for this dataset, achieving an R² of ~0.985 and significantly lower error metrics than both Linear Regression and Random Forest.

This project demonstrates the importance of:

- choosing models that align with feature types  
- understanding the limitations of one‑hot encoding  
- establishing a strong baseline before moving to advanced models  
- using modern boosting algorithms for tabular data  

---

## 🚀 7. Future Improvements

- Hyperparameter tuning for CatBoost  
- SHAP value analysis for deeper interpretability  
- Add interaction features (e.g., age × mileage)  
- Reduce high‑cardinality categories using target encoding  
- Incorporate geographic or market‑based features  
- Deploy the model as an API or dashboard  

---

## 📦 Dataset Access & Usage

This project uses the **Craigslist Vehicle Dataset** from Kaggle.  
Because GitHub does not allow uploading very large files (over 100 MB), the full dataset is **not included** in this repository.

Instead, you can download it directly from Kaggle using the link or the Kaggle API.

### 🔗 Dataset Source
**Craigslist Vehicle Dataset**  
https://www.kaggle.com/code/mohanadyehia49/car-price-prediction-on-craigslist-cars-dataset/input

---

## 📁 Repository Contents

- `vehicle-price-prediction.ipynb` — full analysis and modeling workflow  
- `README.md` — project overview  
