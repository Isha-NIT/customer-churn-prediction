
# 📘 Customer Churn Prediction (ML Project)

A machine learning project to predict customer churn (exit status) for a financial institution based on customer demographics and account information.

---

## 🧠 Objective

Build a predictive model to determine whether a customer will **exit** (`exit_status = 1`) or **stay** (`exit_status = 0`) using features such as age, credit score, balance, number of products, etc.

---

## 📁 Project Structure

```
customer-churn-prediction/
│
├── data/
│   └── customer_exit_status_data.csv        # Input dataset
│
├── notebooks/
│   └── customer_churn_prediction.ipynb      # Main notebook
|
├── README.md                                # Project overview
└── LICENSE                                  # MIT License
```

---

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/Isha-NIT/customer-churn-prediction.git
cd customer-churn-prediction
```

2. Install the dependencies:

```bash
pip install -r requirements.txt
```

---

## 🗃️ Dataset

- File: `customer_exit_status_data.csv`
- Size: ~90,000 rows
- Target variable: `exit_status` (0 or 1)

---

## 📊 EDA Highlights

- Checked for missing values and duplicates
- Handled outliers using IQR method
- Visualized feature relationships with correlation heatmaps and boxplots
- Found class imbalance in target → handled using SMOTE

---

## 🧼 Preprocessing Pipeline

- Used `Pipeline` and `ColumnTransformer`
- Numerical features:
  - Imputation: Mean/Median
  - Scaling: Standard/MinMax
- Categorical features:
  - Imputation: Mode
  - Encoding: One-hot
- Dropped irrelevant columns: `id`, `customer_id`, `last_name`

---

## 🤖 Models Trained

- Logistic Regression  
- Random Forest  
- Gradient Boosting  
- AdaBoost  
- Gaussian Naive Bayes  
- XGBoost  
- LightGBM  

All models trained using:

- Preprocessing pipeline
- SMOTE for imbalance
- Metrics: Precision, Recall, F1 Score

---

## 🔧 Hyperparameter Tuning

Used `RandomizedSearchCV` for:

- Gradient Boosting
- XGBoost
- LightGBM

Settings:

- 3-fold cross-validation
- F1 score optimization
- Best models evaluated on test set

---

## 🏁 Final Evaluation

| Model      | F1 Score | Precision | Recall |
|------------|----------|-----------|--------|
| XGBoost    | 0.6411   | 0.6257    | 0.6573 |
| LightGBM   | 0.6409   | 0.6330    | 0.6491 |

---

## ✅ Key Takeaways

- Product count, age, and account balance were top churn indicators
- SMOTE helped mitigate class imbalance effectively
- XGBoost performed best after tuning


## 📃 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Contributions

Feel free to fork, submit PRs, or open issues. Contributions are welcome!

---

## 📬 Contact

Created by **Isha K S**  
Email: ishaks1995@gmail.com  
GitHub: [github.com/Isha-NIT](https://github.com/Isha-NIT)
