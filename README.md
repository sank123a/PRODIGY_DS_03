# PRODIGY_DS_03
predict whether a customer will purchase a product or service based on their demographic and behavioral data

# 🏦 Bank Marketing Dataset – Decision Tree Classifier

This project builds a **Decision Tree Classifier** to predict whether a customer will **subscribe to a term deposit** based on their demographic and behavioral attributes, using the **Bank Marketing Dataset** from the UCI Machine Learning Repository.

---

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository – Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
- **File Used**: `bank-full.csv`
- **Records**: ~45,000
- **Target Variable**: `y` (binary: `yes` / `no` – did the client subscribe to a term deposit?)

---

## 🧰 Tools and Libraries

- **Python 3**
- **Pandas** – data manipulation
- **Scikit-learn** – machine learning
- **Matplotlib** – data visualization
- **LabelEncoder** – encoding categorical features

---

## 🔄 Process Overview

### 1. **Data Loading**
- Loaded `bank-full.csv` using `pandas.read_csv()`
- Handled semicolon (`;`) as delimiter

### 2. **Data Preprocessing**
- Label-encoded categorical variables using `LabelEncoder`
- Converted target variable `y` to binary (1 = yes, 0 = no)
- Separated features (`X`) and target (`y`)
- Performed train-test split (70% training, 30% testing)

### 3. **Model Building**
- Trained a **Decision Tree Classifier** using entropy (information gain) as the splitting criterion
- Controlled depth using `max_depth=5` to avoid overfitting

### 4. **Model Evaluation**
- Measured accuracy, confusion matrix, and classification report
- Visualized the decision tree using `sklearn.tree.plot_tree()`

---

## 📊 Key Insights

1. **Target Imbalance**:
   - Most customers did **not** subscribe to the term deposit (class imbalance).

2. **Top Predictors**:
   - `duration` (last contact duration)
   - `poutcome` (outcome of the previous marketing campaign)
   - `age` and `job` also contributed significantly

3. **Model Accuracy**:
   - Achieved approximately **88% accuracy** on the test set with depth-limited tree

4. **Overfitting Control**:
   - Restricted tree depth and used entropy to prevent overfitting and improve interpretability

---

## 📁 Folder Structure

```

Bank-Marketing-Classifier/
│
├── bank-full.csv                  # Original dataset
├── bank\_marketing\_decision\PRODIGY_DS_03.ipynb  # Jupyter Notebook with full implementation
├── README.md                      # Project summary and insights

```

---

## ✅ Future Work

- Implement **Random Forest or XGBoost** for improved performance
- Perform **feature engineering** (e.g., age groups, job category)
- Apply **GridSearchCV** for hyperparameter tuning
- Address **class imbalance** using SMOTE or class weights


## 🙌 Acknowledgements

- Data from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing)


