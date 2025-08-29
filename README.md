
# 🏦 Bank Marketing Classifier Comparison

## 📌 Overview  
This project compares the performance of four classification algorithms—K-Nearest Neighbors, Logistic Regression, Decision Trees, and Support Vector Machines—on a real-world marketing dataset from a Portuguese bank. The goal is to predict whether a client will subscribe to a term deposit, enabling smarter targeting and resource allocation.

## 📂 Dataset  
- **Source:** [UCI Machine Learning Repository – Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing)  
- **Records:** Direct marketing campaign data collected via phone calls  
- **Target Variable:** `y` – whether the client subscribed to a term deposit (`yes`/`no`)

### 🔍 Key Features  
- **Client Info:** `age`, `job`, `marital`, `education`, `default`, `housing`, `loan`  
- **Campaign Contact:** `contact`, `month`, `day_of_week`, `duration`  
- **Campaign History:** `campaign`, `pdays`, `previous`, `poutcome`  
- **Economic Indicators:** `emp.var.rate`, `cons.price.idx`, `cons.conf.idx`, `euribor3m`, `nr.employed`  

> ⚠️ Note: The `duration` feature was excluded to avoid data leakage, as it’s only known after the call.

## 🎯 Objective  
Build a predictive model that identifies potential subscribers, improving marketing efficiency and ROI.

## 🧪 Methodology  

### 1. Data Preparation  
- Loaded with `pandas`  
- Cleaned and explored for missing values and data types  

### 2. Feature Engineering  
- Categorical encoding: One-Hot and Target Encoding  
- Numerical scaling: `StandardScaler`  
- Excluded `duration` for realistic modeling  

### 3. Train/Test Split  
- Stratified split to preserve class distribution  

### 4. Baseline Model  
- Majority class prediction to establish baseline accuracy  

### 5. Initial Model Training  
- Algorithms: KNN, Logistic Regression, Decision Tree, SVM  
- Metrics: Accuracy, Precision, Recall, F1-score, ROC AUC  

### 6. Hyperparameter Tuning  
- Grid Search with cross-validation  
- Optimized for ROC AUC  

### 7. Handling Class Imbalance  
- Applied Random Oversampling and Undersampling  

### 8. Re-evaluation  
- Compared model performance across original, oversampled, and undersampled data  

### 9. Performance Visualization  
- Plotted metrics to compare models across scenarios  

## 📈 Results & Insights  

| Model               | Accuracy | Precision | Recall | F1-score | ROC AUC |
|--------------------|----------|-----------|--------|----------|---------|                                   
| Logistic Regression| 0.6010     0.1587       0.5958  0.2506      0.6497
| Decision Tree      | 0.6393    | 0.1608    | 0.5265  | 0.2463    |0.6345   |
| KNN                | 0.7507    | 0.2801     | 0.2011   | 0.2011     |0.5797    |


### 🔍 Key Takeaways  
- Class imbalance significantly impacted model performance  
- Resampling improved Recall but often reduced Precision  
- Hyperparameter tuning enhanced ROC AUC across models  
- Best model depends on business priorities: Recall vs. Precision vs. F1-score  

## ✅ Conclusion  
This project demonstrates the importance of thoughtful preprocessing, tuning, and evaluation when working with imbalanced datasets. By comparing multiple classifiers and resampling strategies, we gain actionable insights into how to optimize predictive performance for real-world marketing applications.


---

Want help writing the `requirements.txt`, organizing your code into modules, or creating visuals for the README? I can help you polish this into a standout portfolio piece.
