# 🧠 Customer Churn Prediction

## 👋 Kickoff: Churn Dataset Loaded
The **Churn_Modelling.csv** dataset has been loaded, previewed, and analyzed for churn balance.
---

### 📋 Sample Data Preview

| RowNumber | CustomerId | Surname  | CreditScore | Geography | Gender | Age | Tenure | Balance | NumOfProducts | HasCrCard | IsActiveMember | EstimatedSalary | Exited |
|------------|-------------|----------|--------------|------------|---------|-----|---------|----------|----------------|------------|----------------|----------------|---------|
| 1 | 15634602 | Hargrave | 619 | France | Female | 42 | 2 | 0.00 | 1 | 1 | 1 | 101348.88 | 1 |
| 2 | 15647311 | Hill | 608 | Spain | Female | 41 | 1 | 83807.86 | 1 | 0 | 1 | 112542.58 | 0 |
| 3 | 15619304 | Onio | 502 | France | Female | 42 | 8 | 159660.80 | 3 | 1 | 0 | 113931.57 | 1 |
| 4 | 15701354 | Boni | 699 | France | Female | 39 | 1 | 0.00 | 2 | 0 | 0 | 93826.63 | 0 |
| 5 | 15737888 | Mitchell | 850 | Spain | Female | 43 | 2 | 125510.82 | 1 | 1 | 1 | 79084.10 | 0 |

---

## 📊 Churn Distribution

| Class | Count | Proportion |
|--------|--------|-------------|
| 0 (Retained) | 7963 | 0.7963 |
| 1 (Churned) | 2037 | 0.2037 |

The dataset shows that about **20% of customers have churned**, indicating **class imbalance**.

---

## ⚡ Quick Take
- Dataset is clean and well-structured.  
- Binary target variable: `Exited` (0 = retained, 1 = churned).  
- Slightly imbalanced (approx. 4:1).  
- Imbalance will be handled via **stratified sampling** and **class weighting** during model training.  

---

## 🔍 Next Steps
### 1. Exploratory Data Analysis (EDA)
Segment churn by:
- Geography  
- Gender  
- Age  
- Tenure  
- Number of Products  
- Balance  
- Customer Activity  

### 2. Feature Engineering & Preparation
- One-hot encode categorical variables  
- Scale numeric variables  
- Split data into stratified **train/validation** sets  

### 3. Baseline Modeling
- **Logistic Regression** (with `class_weight='balanced'`)  
- **XGBoost / LightGBM** (for stronger tree-based modeling)  

### 4. Model Evaluation Metrics
- **ROC-AUC**
- **Precision-Recall AUC**
- **Confusion Matrix**
- **Lift and Decile Analysis**

### 5. Model Interpretability
- **Feature Importance**
- **SHAP Analysis** (to identify top churn drivers)

---

## 🧾 Deliverables
- Exploratory analysis visuals and summaries  
- Model performance metrics and plots  
- Feature importance and SHAP charts  
- Scored dataset file (`churn_val_scored.csv`)  
- (Optional) Model deployment or dashboard notebook  

---

## 🛠️ Tech Stack
| Component | Tool |
|------------|------|
| Language | Python 3.x |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Modeling | Scikit-Learn, XGBoost, LightGBM |
| Interpretability | SHAP |
| Evaluation | ROC-AUC, PR-AUC, Lift Charts |

---

## 📂 Project Structure
├── data/
│ └── Churn_Modelling.csv
├── notebooks/
│ └── churn_analysis.ipynb
├── models/
│ └── churn_model.pkl
├── outputs/
│ └── churn_val_scored.csv
├── README.md
└── requirements.txt

yaml
Copy code

---

## 📈 Example Visualization (EDA)
<img width="1000" height="800" alt="image" src="https://github.com/user-attachments/assets/94229ca4-fd81-47c8-a9ec-698d177d53e8" />

---

## 🚀 Future Enhancements
- Add hyperparameter tuning (GridSearch / Optuna)
- Implement SMOTE or ADASYN oversampling
- Deploy model as REST API (Flask/FastAPI)
- Integrate Power BI / Streamlit dashboard

---

## 🤝 Contributing
Pull requests are welcome!  
For major changes, please open an issue first to discuss what you’d like to improve.

---

## 🧑‍💻 Author
**Chaitali Mali**  
📧 chaitalimali902@gmail.com.com  
💼 [LinkedIn(https://www.linkedin.com/in/chaitalimali/) | 🌐 [GitHub](https://github.com/Chaitali-mali)

---

### ⭐ If you found this project helpful, please consider giving it a star on GitHub!

