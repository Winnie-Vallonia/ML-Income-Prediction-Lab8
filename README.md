## 🧠 Predicting Income Levels with Census Data

This project is part of **Lab 8: Define and Solve an ML Problem of Your Choosing** for my machine learning course with Break Through Tech.

### 📊 Problem Statement

Using U.S. Census data from 1994, the goal is to predict whether a person's income exceeds \$50,000 per year based on demographic and work-related features.

This is a **supervised binary classification** problem. The label is `income_binary`, which indicates whether income is `<=50K` or `>50K`.

---

### 📁 Data Used

* **Dataset:** `censusData.csv`
* The dataset includes features like:

  * Age
  * Education
  * Occupation
  * Capital gain/loss
  * Hours worked per week
  * Native country
  * Many others (after one-hot encoding)

---

### ⚙️ Machine Learning Pipeline

**1. Data Preprocessing**

* Handled missing values with median/mode
* One-hot encoded categorical variables
* Removed outliers using capping (clip)
* Dropped irrelevant features (e.g., `fnlwgt`)

**2. Modeling**

* Started with **Logistic Regression**
* Tried **Random Forest**
* Tuned hyperparameters using **GridSearchCV**

**3. Evaluation Metrics**

* Accuracy
* Log Loss

---

### ✅ Results

| Model                     | Accuracy   | Log Loss  |
| ------------------------- | ---------- | --------- |
| Logistic Regression       | 84.39%     | 0.335     |
| Untuned Random Forest     | 83.68%     | 0.556     |
| ✅ **Tuned Random Forest** | **85.34%** | **0.315** |

The **tuned Random Forest** performed best after hyperparameter optimization.

---

### 📚 What I Learned

* Logistic regression can outperform more complex models on certain structured datasets
* Hyperparameter tuning significantly boosts performance
* One-hot encoding can lead to high dimensionality, but tree-based models handle it well

---

### 👤 Author

**Winnie Nna**
