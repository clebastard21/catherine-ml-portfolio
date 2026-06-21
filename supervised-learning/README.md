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
- Encoded categorical variables using one‑hot encoding  
- Scaled numerical features  
- Split data into training and testing sets  

---

## 🤖 3. Models Trained

### **Linear Regression**
- Simple, interpretable baseline model  
- Works well with high‑dimensional one‑hot encoded data  

### **Random Forest Regressor**
- Nonlinear ensemble model  
- In theory captures interactions and complex relationships  

---

## 📈 4. Model Performance

| Model | MAE | RMSE | R² |
|-------|---------|-----------|---------|
| **Linear Regression** | 6036 | 8831 | **0.633** |
| **Random Forest** | 10964 | 14036 | **0.074** |

**Linear Regression significantly outperformed Random Forest**, indicating that the dataset is largely linear and that high‑cardinality categorical variables make tree‑based models struggle.

---

## 🔍 5. Key Insights

- Newer vehicles and lower mileage strongly increase price  
- Condition and manufacturer are major value drivers  
- Trucks, SUVs, and AWD/4WD vehicles tend to be priced higher  
- Simpler models can outperform complex ones when data structure is linear  

---

## 📝 6. Conclusion

Linear Regression proved to be the most effective model for this dataset, achieving an R² of ~0.63.  
Random Forest performed poorly due to the extremely high‑dimensional one‑hot encoded feature space.

This project demonstrates the importance of:
- establishing a strong baseline model  
- understanding data structure  
- choosing models that align with feature types  

---

## 🚀 7. Future Improvements

- Try CatBoost or LightGBM (handle categorical data natively)  
- Add interaction features (e.g., year × mileage)  
- Reduce high‑cardinality categories using target encoding  
- Tune hyperparameters for improved performance  
- Incorporate geographic or market‑based features  

---

## 📁 Repository Contents

- `notebook.ipynb` — full analysis and modeling workflow  
- `data/` — cleaned dataset (if allowed)  
- `README.md` — project overview  
