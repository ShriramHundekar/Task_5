# Task_5
Heart disease classification using Decision Tree and Random Forest with evaluation metrics and visualizations
# ❤️ Heart Disease Prediction using Decision Tree & Random Forest

This project applies **tree-based machine learning models** — Decision Tree and Random Forest — to classify whether a person is likely to have **heart disease**, based on several medical attributes.

This work was completed as part of **Task 5** in an **AI & ML Internship Program**.

---

## Dataset Description

- **Dataset File**: `heart.csv`
- **Total Instances**: 303
- **Target Column**: `target` (1 = has heart disease, 0 = no heart disease)

###Features Used:
| Feature | Description |
|---------|-------------|
| `age` | Age of the patient |
| `sex` | Gender (1 = male, 0 = female) |
| `cp` | Chest pain type |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol |
| `fbs` | Fasting blood sugar > 120 mg/dl |
| `restecg` | Resting ECG results |
| `thalach` | Max heart rate achieved |
| `exang` | Exercise-induced angina |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of ST segment |
| `ca` | Number of major vessels colored by fluoroscopy |
| `thal` | Thalassemia type |
| `target` | 1 = disease, 0 = no disease ✅ |

---

##Objectives

- Load and clean the dataset
- Split into training and testing sets
- Train a **Decision Tree Classifier**
- Train a **Random Forest Classifier**
- Evaluate both models using:
  - Accuracy
  - Confusion Matrix
  - Precision, Recall, F1-Score
  - Cross-validation scores
- Visualize:
  - Decision Tree structure
  - Feature importances in Random Forest

---

##Tools and Libraries Used

- Python 3.x
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn (`DecisionTreeClassifier`, `RandomForestClassifier`)
- Jupyter Notebook

---

##Workflow Summary

### Step 1: Load Dataset
- Loaded using Pandas from `heart.csv`
- Checked for missing values (none present)

###  Step 2: Preprocessing
- No encoding required — dataset is clean
- Features (`X`) and label (`y`) separated

###  Step 3: Train-Test Split
- Used `train_test_split()` from scikit-learn with 80/20 split

###  Step 4: Decision Tree Classifier
- Trained with `max_depth=4` to avoid overfitting
- Evaluated using:
  - Accuracy score
  - Confusion Matrix
  - Classification Report
- Visualized the tree using `plot_tree()`

###  Step 5: Random Forest Classifier
- Trained with 100 trees (`n_estimators=100`)
- Evaluated with same metrics
- Feature importances plotted using bar chart

###  Step 6: Cross-validation
- Used `cross_val_score()` with 5-fold CV
- Compared CV accuracy of both models

---

##Model Performance

| Model | Test Accuracy | CV Accuracy |
|-------|---------------|-------------|
| Decision Tree | ~81% | ~79% |
| Random Forest | ~85% | ~84% |

 **Random Forest outperformed Decision Tree** on both test set and CV, and is more robust due to ensemble learning.

---

##Files Included

| File Name | Description |
|-----------|-------------|
| `Heart_DecisionTree_RandomForest.ipynb` | Jupyter notebook with all code, outputs, and plots |
| `heart.csv` | Heart disease dataset |
| `README.md` | This documentation file |

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/heart-disease-decisiontree-randomforest.git
   cd heart-disease-decisiontree-randomforest
