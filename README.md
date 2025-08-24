# 🌱 Predictive Modeling for Agriculture

This project applies machine learning to soil measurement data in order to classify the optimal crop type.  
The work was completed as part of a DataCamp project on predictive modeling.

---

## 📖 Problem Statement
Farmers rely on soil measurements (nitrogen, phosphorous, potassium, pH) to decide which crop will grow best.  
The goal of this project is to identify **which single soil feature is the strongest predictor** for crop type.

---

## 📊 Dataset
The dataset (`soil_measures.csv`) contains:
- `N`: Nitrogen content ratio in the soil  
- `P`: Phosphorous content ratio in the soil  
- `K`: Potassium content ratio in the soil  
- `pH`: Acidity/alkalinity of the soil  
- `crop`: Target variable, categorical crop type  

Each row represents soil conditions in a field and the corresponding optimal crop.

---

## 🛠️ Approach
1. **Exploratory Data Analysis (EDA):**
   - Loaded the dataset with `pandas`
   - Inspected distributions and correlations between soil features

2. **Modeling:**
   - Used **Logistic Regression** from `scikit-learn`
   - Trained separate models for each feature (`N`, `P`, `K`, `pH`) individually
   - Split the data using `train_test_split`

3. **Evaluation:**
   - Measured predictive power with **accuracy score**
   - Compared feature-level performances to identify the best predictor

---

## ✅ Key Results
- **Potassium (`K`)** was found to be the **most predictive feature** for crop classification.  
- Achieved an accuracy score of **~0.27** when using `K` alone as input.

Example output:
```python
{'K': 0.2667}
