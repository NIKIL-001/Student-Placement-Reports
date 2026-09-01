# Student-Placement-Reports
# 🎓 Student Placement Prediction — Classification & Regression

![Python](https://img.shields.io/badge/Python-3.12-blue)
![ML](https://img.shields.io/badge/Machine%20Learning-Sklearn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-yellow)

---

## 📌 Project Overview

This project predicts **student placement outcomes** and **salary packages** using Machine Learning. It is a dual-task project combining both **Classification** (Placed / Not Placed) and **Regression** (Salary Package in LPA) on real-world student academic and personal data.

We got the students datas with their academic, technical, and career-related attributes and each of the student has unique records and has shown their intrest in different areas, Therefor now we will be helping the collage by providing them an proper data-driven career guidance and trainig design and finally how to improve Placement with high paying job.

Built entirely in **Google Colab** using Python and scikit-learn.

---

## 🎯 Objectives

- Predict whether a student will be **placed or not placed** (Classification)
- Predict the **salary package** for placed students (Regression)
- Compare multiple ML algorithms and evaluate their performance

---

## 📂 Dataset Description

| Property | Details |
|---|---|
| Total Records | 5034 rows |
| Total Features | 26 columns |
| Target 1 | `placement_status` (Placed / Not Placed) |
| Target 2 | `salary_package_lpa` (Salary in LPA) |

### 📋 Features

| # | Feature | Type | Description |
|---|---|---|---|
| 1 | student_id | int | Unique student identifier (dropped) |
| 2 | age | int | Age of student |
| 3 | gender | object | Male / Female |
| 4 | cgpa | float | Cumulative GPA |
| 5 | branch | object | Engineering branch (CS, ECE, ME...) |
| 6 | college_tier | object | Tier 1 / Tier 2 / Tier 3 |
| 7 | internships_count | int | Number of internships |
| 8 | projects_count | int | Number of projects |
| 9 | certifications_count | int | Number of certifications |
| 10 | coding_skill_score | float | Coding skill score |
| 11 | aptitude_score | float | Aptitude test score |
| 12 | communication_skill_score | float | Communication score |
| 13 | logical_reasoning_score | float | Logical reasoning score |
| 14 | hackathons_participated | int | Number of hackathons |
| 15 | github_repos | int | Number of GitHub repositories |
| 16 | linkedin_connections | int | LinkedIn connections count |
| 17 | mock_interview_score | float | Mock interview score |
| 18 | attendance_percentage | float | Attendance percentage |
| 19 | backlogs | int | Number of backlogs |
| 20 | extracurricular_score | float | Extracurricular activity score |
| 21 | leadership_score | float | Leadership score |
| 22 | volunteer_experience | object | Yes / No |
| 23 | sleep_hours | float | Average sleep hours |
| 24 | study_hours_per_day | float | Study hours per day |
| 25 | placement_status | object | **Target — Classification** |
| 26 | salary_package_lpa | float | **Target — Regression** |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.12 | Programming Language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Scikit-learn | ML models and evaluation |
| Statsmodels | Logistic Regression with summary |
| Matplotlib / Seaborn | Data visualization |
| Google Colab | Development platform |

---

## ⚙️ Project Workflow

```
1. Data Loading & Exploration
        ↓
2. Data Cleaning (Handle Missing Values)
        ↓
3. Feature Separation (X and Y)
        ↓
4. Encoding Categorical Variables (One Hot Encoding + Label Encoding)
        ↓
5. Train Test Split (80% Train / 20% Test)
        ↓
6. Classification Models (Placement Status)
   ├── Logistic Regression
   ├── Decision Tree Classifier
   └── XGBoost Classifier
        ↓
7. Regression Models (Salary Package)
   ├── Random Forest Regression
   ├── XGBoosting Regressor
   └── Gradient Boosting Regressor
        ↓
8. Model Evaluation & Comparison
```

---

## 🤖 Models Used

### Classification — Placement Status

| Model | Metrics Used |
|---|---|
| Logistic Regression | Accuracy, Confusion Matrix, Classification Report |
| Decision Tree Classifier | Accuracy, Confusion Matrix, Classification Report |
| XGBoost Classifier | Accuracy, Confusion Matrix, Classification Report |

### Regression — Salary Package

| Model | Metrics Used |
|---|---|
| Random Forest Regressor | R2 Score, MAE, MSE, RMSE |
| XGBoosting Regressor | R2 Score, MAE, MSE, RMSE |
| Gradient Boosting Regressor | R2 Score, MAE, MSE, RMSE |

---

## 📊 Evaluation Metrics

### Classification
- **Accuracy Score** — Overall correct predictions
- **Confusion Matrix** — True Positives, False Positives, True Negatives, False Negatives
- **Classification Report** — Precision, Recall, F1-Score, Support

### Regression
- **R2 Score** — How well model explains salary variation (closer to 1 is better)
- **MAE** — Mean Absolute Error in salary prediction
- **MSE** — Mean Squared Error (Penalizes large errors )
- **RMSE** — Root Mean Squared Error (Brings back to original unit (LPA))

---

## 🔄 Data Preprocessing Steps

1. **Dropped irrelevant columns** — `student_id`, `CASENUM`
2. **Handled missing values** — Filled with mean for numeric columns
3. **One Hot Encoding** — Applied on `gender`, `branch`, `college_tier`, `volunteer_experience`
4. **Label Encoding** — Applied on `placement_status` (Placed=1, Not Placed=0)
5. **Type conversion** — All features converted to `float64`
6. **Filtered placed students** — For regression, only placed student data was used

---

## 📁 Repository Structure

```
student-placement-prediction/
│
├── education.csv                  # Dataset
├── student_placement.ipynb        # Main Colab Notebook
├── README.md                      # Project Documentation
└── requirements.txt               # Required packages
```

---

## 🚀 How to Run

**1. Clone the Repository**
```bash
git clone https://github.com/your-username/student-placement-prediction.git
```

**2. Upload to Google Colab**
- Go to [Google Colab](https://colab.research.google.com)
- Upload `student_placement.ipynb`
- Upload `education.csv` to `/content/`

**3. Install Required Packages**
```bash
pip install -r requirements.txt
```

**4. Run All Cells**
- Runtime → Run All

---

## 📦 Requirements

```
pandas
numpy
scikit-learn
statsmodels
matplotlib
seaborn
xgboost
```

---

## 💡 Key Insights

- **CGPA, aptitude score, and coding skill score** are the strongest predictors of placement
- **Branch and college tier** significantly impact both placement status and salary
- **Students with internships and projects** have a higher probability of placement
- **Random Forest Regressor** gives the best salary prediction accuracy among regression models
- **Two-stage modelling approach** — first predict placement, then predict salary for placed students — gives the most logical and accurate results

---

## 👨‍💻 Author

**Nikil**
- Final Year B.E. Computer Science Engineering (Data Science Specialization)
- Chennai, India
---








This project is open source and available under the [MIT License](LICENSE).
