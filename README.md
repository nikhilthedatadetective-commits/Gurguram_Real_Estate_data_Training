# Gurugram Real Estate Price Prediction – Data Training Repository  

##  Project Overview  
This repository focuses on **data preprocessing, feature engineering, exploratory analysis, and machine learning model training** for predicting real estate prices in Gurugram.  
The dataset was collected via **web scraping from 99acres.com** for both **flats** and **houses**, cleaned, merged, and transformed into a structured format.  
Multiple ML models and encoding strategies were tested to identify the most accurate price prediction model.  

👉 The **deployment** part of this project is available in a separate repository: [Gurguram_Real_Estate](#).  

---

##  Dataset Description  
- **Source**: Web scraped from 99acres.com  
- **Raw size**: ~4000 records (after cleaning → **3635 records**)  
- **Features collected**:  
  - Property Type (Flat / House)  
  - Sector & Location Info  
  - Built-up Area  
  - Price & Price per sqft  
  - Balcony, Furnishing Type, Age of Property  
  - Latitude & Longitude (geo-coordinates)  
  - And more property-specific features  

---

##  Workflow / Pipeline  
1. **Data Collection** – Scraping real estate data from 99acres  
2. **Data Preprocessing** – Cleaning, handling missing values, merging datasets  
3. **EDA**  
   - Univariate & Multivariate analysis  
   - Pandas Profiling Reports  
   - Data Visualization (Seaborn, Matplotlib)  
4. **Feature Engineering & Selection**  
   - Ordinal Encoding, One-Hot Encoding, Target Encoding  
   - PCA-based dimensionality reduction (experiment)  
5. **Outlier Treatment**  
6. **Baseline Modeling**  
   - Linear Regression, Ridge, LASSO, SVR, Decision Tree, Random Forest, Extra Trees, Gradient Boosting, AdaBoost, XGBoost, MLP  
7. **Model Selection & Comparison**  
   -  **Best Results:**  
     - **Target Encoding + Random Forest → R²: 0.90, MAE: 0.44**  
     - **Random Forest with Hyperparameter Tuning** chosen as final model  
8. **Export Artifacts** – Trained model & transformations saved as `.pkl`  

---

##  Tech Stack  
- **Programming Language**: Python 3  
- **Libraries & Tools**:  
  - Data Handling → Pandas, NumPy  
  - Visualization → Matplotlib, Seaborn  
  - EDA Automation → Pandas Profiling  
  - Feature Engineering → Scikit-learn, Category Encoders  
  - Machine Learning → Scikit-learn, XGBoost  
  - Model Persistence → Pickle  

---

## 📈 Results Summary  

| Encoding Strategy | Best Model        | R² Score | MAE   |  
|-------------------|------------------|----------|-------|  
| Ordinal Encoding  | XGBoost          | 0.889    | 0.50  |  
| One-Hot Encoding  | Extra Trees      | 0.896    | 0.46  |  
| PCA + One-Hot     | Random Forest    | 0.763    | 0.64  |  
| Target Encoding   |  Random Forest   | **0.905**| **0.44** |  

✅ Final model selected: **Random Forest Regressor (with GridSearchCV tuning)**  

---
## Thank You


