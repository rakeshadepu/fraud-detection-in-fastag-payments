# Fraud-detection-in-fastag-payments

# FASTag Fraud Detection System

### Machine Learning–Based Fraud Detection with Streamlit Dashboard

---

## Project Overview

FASTag is an electronic toll collection system used across India to enable seamless toll payments. While it improves efficiency, the system is also vulnerable to **fraudulent activities** such as:

* Amount mismatches
* Vehicle misuse
* Abnormal speed or transaction behavior
* Repeated suspicious transactions

This project implements an **end-to-end fraud detection system** using **Machine Learning** and an **interactive Streamlit web application** to:

* Detect fraudulent FASTag transactions
* Compare multiple ML models
* Provide real-time statistics and visual analytics
* Support both **manual input** and **CSV-based batch prediction**

---

## Key Features

* End-to-end ML pipeline (data → model → deployment)
* Streamlit-based interactive frontend
* Manual & bulk (CSV) fraud prediction
* Multiple ML model comparison
* Real-time & historical transaction analytics
* Visual dashboards for fraud insights

---

## Machine Learning Pipeline

### 1. Data Preprocessing & Feature Engineering

* Amount mismatch: `Transaction_Amount − Amount_paid`
* Vehicle profile generation
* High-speed anomaly detection
* Date, time, day, and month extraction
* One-hot encoding for categorical variables

### 2. Models Implemented

* Logistic Regression
* Decision Tree
* Random Forest *(final selected model)*
* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)

### 3. Model Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

> **Random Forest** performed best and is used for deployment.

---

## Streamlit Application Modules

### Home

* Manual transaction input
* CSV upload for batch predictions
* Fraud / Not Fraud classification

### Models

* Model training & evaluation
* Performance comparison
* Confusion matrix visualizations

### Real-Time Statistics

* NETC monthly & yearly transaction trends
* RBI & NPCI-related insights
* Distribution, trend, and correlation analysis

### Statistics Dashboard

* State-wise, day-wise, month-wise fraud analysis
* KDE plots, histograms, regression plots
* Fraud percentage visualization

---

## Project Structure

```text
Fraud-detection-in-fastag-payments/
│
├── data/                         # Datasets (CSV files)
├── Documentation/                # Project documentation
├── notebooks/                    # Jupyter notebooks (EDA & experiments)
│
├── app.py                        # Streamlit application entry point
├── model.py                      # ML models & evaluation logic
├── prediction.py                 # Prediction utilities
├── stats.py                      # Statistical analysis & plots
├── live_stats.py                 # Real-time data visualization
│
├── random_forest_model.joblib    # Trained ML model
├── model_features.joblib         # Model feature list
├── label_encoders.joblib         # Encoders
│
├── README.md                     # Project documentation
└── requirements.txt              # Python dependencies
```

---

## 🛠️ Technologies Used

* **Programming Language:** Python
* **Frontend:** Streamlit
* **Machine Learning:** Scikit-learn
* **Data Analysis:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Model Persistence:** Joblib
* **Version Control:** Git & GitHub

---

## How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/rakeshadepu/Fraud-detection-in-fastag-payments.git
cd Fraud-detection-in-fastag-payments
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Streamlit App

```bash
streamlit run app.py
```

### Open Browser

```text
http://localhost:8501
```

---

## Output & Results

* Accurate detection of fraudulent transactions
* Clear visual insights into fraud patterns
* Model comparison for informed selection
* Scalable structure for real-world deployment

---

## Future Enhancements

* Real-time transaction streaming
* Deep learning models (LSTM / Autoencoders)
* API-based deployment
* Dockerized application
* Advanced anomaly detection techniques

---

## Author

**Rakesh Adepu**
Master’s Aspirant in Data Science
GitHub: [https://github.com/rakeshadepu](https://github.com/rakeshadepu)

---

## License

This project is intended for **academic and educational purposes**.

---
