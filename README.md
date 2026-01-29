# 🚗 Car Price Prediction using Machine Learning

This project focuses on predicting **used car prices** based on features such as **car name, company, year, kilometers driven, and fuel type**.  
The dataset was collected from **Quikr**, containing real-world noisy data that required extensive cleaning and preprocessing before model training.

---

## 📌 Project Overview

- **Goal:** Predict the selling price of used cars  
- **Problem Type:** Regression  
- **Algorithm Used:** Linear Regression  
- **Evaluation Metric:** R² Score  
- **Final R² Score:** ~0.57  

---

## 📂 Dataset Information

- **Source:** Quikr Car Dataset  
- **Initial Size:** 892 rows × 6 columns  
- **Final Cleaned Size:** 815 rows × 6 columns  

### Features

| Column Name | Description |
|------------|------------|
| name | Car model name |
| company | Manufacturer |
| year | Manufacturing year |
| kms_driven | Distance driven |
| fuel_type | Petrol / Diesel / LPG |
| Price | Target variable (INR) |

---

## ⚠️ Data Quality Issues

- Inconsistent car names  
- Non-numeric values in `year`  
- "Ask For Price" values in `Price`  
- Commas in numeric fields  
- Text values in `kms_driven`  
- Missing values in `fuel_type`  
- Price outliers  

---

## 🧹 Data Cleaning & Preprocessing

- Cleaned car names (kept first 3 meaningful words)
- Removed rows with "Ask For Price"
- Converted `Price` to integer
- Cleaned and converted `kms_driven`
- Removed invalid year values
- Handled missing fuel types
- Removed extreme price outliers (`Price < 6,000,000`)
- Saved cleaned data as `car_data.csv`

---

## 🔧 Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 🧠 Machine Learning Pipeline

- OneHotEncoder for categorical features
- Linear Regression model
- Used Pipeline and ColumnTransformer

---

## 📊 Model Evaluation

- Train-Test Split: 80/20
- R² Score: ~0.57

The model explains approximately **57% of the variance** in car prices, which is reasonable for noisy real-world data.

---

## 🔁 Stability Check

- Model trained multiple times
- Consistent R² score observed
- Pipeline ensured no data leakage

---

## 🚀 Future Improvements

- Use advanced models (Random Forest, XGBoost)
- Feature engineering (car age, log price)
- Hyperparameter tuning
- Model deployment using Flask/FastAPI
- Web-based UI

---

## 📁 Project Structure

```
├── quikr_car.csv
├── car_data.csv
├── car_price_prediction.ipynb
├── README.md
```

---
## ✅ Conclusion

This project demonstrates a **complete end-to-end machine learning workflow**, starting from raw data collection to model evaluation.  
Despite working with **noisy, real-world data**, the Linear Regression model achieved a **reasonable R² score of ~0.57**, highlighting the importance of effective data preprocessing.

Key takeaways:
- Real-world datasets require extensive cleaning
- Pipelines help prevent data leakage
- Simple models can still provide meaningful insights

With further improvements, this project can evolve into a **production-ready car price prediction system**.
