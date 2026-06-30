# Healthcare-Billing-Anomaly-Detection-Using-Autoencoders

Data Source: https://www.kaggle.com/datasets/speedoheck/inpatient-hospital-charges

---

## Dataset

The dataset contains inpatient hospital billing records from hospitals across the United States.

Key columns include:
- DRG Definition  
- Provider details (ID, name, state, region)  
- Total Discharges  
- Average Covered Charges  
- Average Total Payments  
- Average Medicare Payments  

Total records: 163,065

---

## Data Cleaning

- Removed duplicate rows  
- Converted currency columns to numeric format  
- Cleaned symbols like `$` and commas  

---

## Feature Engineering


- Charge to Medicare Ratio  
- Payment Gap  
- Payment Gap Ratio  
- Charge per Discharge  
- Log Covered Charges  
- Log Medicare Payments  
- Charge Z-score  
- State Charge Deviation  
- DRG Frequency  
- Regional Cost Ratio  

---

## Exploratory Data Analysis

- Data is highly right-skewed  
- Few hospitals have very high charges  
- Strong outliers present in billing data  
- Large variation across states and regions  
- Engineered features reduce skewness and improve visibility of patterns  

---

## Data Preprocessing

- Train-test split (80/20)  
- One-hot encoding for categorical variables  
- Frequency encoding for high-cardinality columns  
- Feature scaling using StandardScaler  

---

## Models

Three autoencoders were used:

- Basic Autoencoder  
- Deep Autoencoder  
- Tanh Autoencoder  

Basic Autoencoder performed best based on validation loss.

---

## Anomaly Detection

- Reconstruction error calculated using MSE  
- 99th percentile used as threshold  
- Values above threshold marked as anomalies  

---

## Results

- Total records: 32,613  
- Anomalies detected: 327  
- Anomaly percentage: 1%  

---


## Tools Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- TensorFlow / Keras  

---

