# Time Series Forecasting using XGBoost & Prophet 

### 📈 **Objective**: Analyse importer booking patterns and forecast **future PVC imports** based on historical data (April 2019 – June 2025).

This project focuses on **time series forecasting** using two machine learning approaches:  

- **Facebook(Meta) Prophet** – a model designed for capturing trend, seasonality, and holiday effects in time series.  
- **XGBoost Regressor** – a gradient boosting model adapted for regression forecasting using lag features and engineered predictors.  

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=DhyeyPatel30&include_repo=Internship-Project&exclude_repo=DhyeyPatel30,STREET-LIGHT-FAULT-DETECTION-SYSTEM,Tableau-Interactive-Dashboard-EDA,Univariate-Forecasting-using-Prophet,Sales-forecasting-using-SARIMAX,To-do-List-angular,C-lang.-Projects,My.viewport,Amazon_prime_db&layout=compact&theme=dark&card_width=300&hide_border=false&border_color=30363d&border_radius=12)

---

## 📂 Project Structure

    Project_Name/
    │── README.md                 # Project documentation
    │── requirements.txt          # List of dependencies
    │
    │── data/                     # Datasets
    │   ├── raw/                  # Original unmodified dataset
    │   ├── processed/            # Cleaned and preprocessed dataset
    │   ├── hyperparameters/      # Dataset of all the hyperparams  tested
    │   ├── forecasted-output/    # Datasets of forecasted results of   all the models
    │   ├── dashboard/            # Dataset for tableau dashboard
    │
    │── notebooks/                # Jupyter notebooks
    │   ├── combined/             # Notebooks of both models combined
    │   ├── other-notebooks/      # Other notebooks
    │   ├── Prophet/              # Only prophet model notebooks
    │   ├── XGBoost/              # Only xgboost model notebooks
    │
    │── other-assets/             # Extra assets for the project
    │
    │── Tableau-dashboard/        # Tableau dashboard for EDA

---

## 🔄 Machine Learning / Data Science Lifecycle
| Step                                   | Implementation in Project                                                    |
| -------------------------------------- | ---------------------------------------------------------------------------- |
| **1. Problem Definition**              | Forecast future PVC imports (July–Sept 2025).                                |
| **2. Data Collection/Source**                 | Excel sheets                                          |
| **3. Data Preprocessing**              | Data aggregation, categorical encodings, Handling missing value, Weekly resampling.      |
| **4. Exploratory Data Analysis (EDA)** | Correlation Heatmap, Tableau dashboard.                    |
| **5. Feature Engineering**             | Lags (`lag_1`), cost, time-based features(booking date, week number). |
| **6. Model Selection**                 | Prophet (trend/seasonality), XGBoost (short-term regression).                |
| **7. Model Training**                  | Training testing split 80:20 ratio, Prophet fit with `ds, y`; XGBoost with engineered features.                  |
| **8. Model Evaluation**                | MSE, RMSE, MAE,  MAPE, Approx. Accuracy.                                                             |
| **9. Forecasting & Deployment**        | Forecast July–Sept 2025, Tableau dashboard for visualization.                |

## 📊 Dataset  
- **Source**: Excel sheets 
- **Features**:  
  - `date` or `timestamp` column → Date
  - `target` column → import quantity (Fin QTY in MTs) 
  - Additional predictors → Date, Fin CiF ($/MT), Fin QTY (MTs), lag_1, Cost, booking date
- **Size**: Rows: 100128 x Columns: 8, 1st April 2019 - 30th June 2025

   ### **NOTE: Column headers should be consistent as mention: Date, K level, Fin Cif ($/MT), Fin QTY (MTs)**
- Rename as per convention given if needed<br>
   date --> Date<br>
   High K/ Low K --> K level<br>
   Fin Cif (\$/Mt) --> Fin Cif (\$/MT)<br>
   Fin Qty (Mt) --> Fin QTY (MTs)<br>
- change in column headers will lead to 'column not in index' error 
- Also the sheet containing actual dataset should be placed first in the excel workbook.
---

# 🛠️ Methodology  
## 🔹 Data Preprocessing  
- Missing value imputation (mean-fill, dropna)
- Resampling to regular intervals (weekly)  
- Feature engineering (lag features, feature creatation, categorical value encoding)  

### 🔹 Models Implemented  
1. **Prophet**  
   - Decomposes time series into **trend + seasonality + holidays**  
   - Robust to missing values & outliers  

2. **XGBoost**  
   - Gradient boosting on decision trees  
   - Trained using lagged features & engineered predictors  
   - Effective for short-term forecasting  

### 🔹 Evaluation Metrics 
- **MSE** – Mean Squared Error 
- **MAE** – Mean Absolute Error  
- **RMSE** – Root Mean Squared Error  
- **MAPE** – Mean Absolute Percentage Error 
- **Accuracy**(approx.) – 100 - MAPE % 

### 🔹 Future Forecasting  
   1. Future Dates: 1st July 2025 - 30th September 2025
   2. Future date features: Mean, Rolling Mean, Prophet Forecast
 

 ---
## 🚀 How to Run  

####  **Note: Store the aggregated file with column header convention as mentioned in data source section as : 'fin_PVC_dataset.xlsx' in preprocessed data folder**

1. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
2. **Run notebooks step-by-step**
   ```bash
   run '.ipynb' notebooks 
---

## 🛠️ Tech Stack

- Language: Python 3.10.0

- Data Handling: Pandas, NumPy

- Visualization: Matplotlib, Seaborn

- Machine Learning: Scikit-learn, XGBoost, Prophet

- Development: Jupyter Notebook/VS code

---

### 📄 Documentation

- Project ppt: [Presentation](other-assets/DhyeyPatel_intship_ppt.pptx)
- Tableau Dashboard: [Final_dashboard | Dhyey Patel](https://public.tableau.com/views/Final_dashboard_17543813139300/Dashboard13?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)<br><br>

---

**Note: More details and dataset cannot be provided because of confidentiality constrained.**

---

## 👨‍💻 Author

Name: Dhyey Patel

Role: Data Science Intern

Personal Email: dhyeyptl3074@gmail.com

Company Email: dhyey2.patel@ril.com

LinkedIn: [DhyeyPatel30](https://www.linkedin.com/in/DhyeyPatel30/)

GitHub: [DhyeyPatel30](https://github.com/DhyeyPatel30)
