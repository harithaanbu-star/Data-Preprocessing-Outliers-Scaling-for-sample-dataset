# Data Preprocessing Practice
# 🚀 Day 3 — AI Internship Journey

## 📌 Project Overview
This repository contains my Day 3 learning progress during my AI Internship.
I explored end-to-end **Data Preprocessing** techniques using a sample Employee dataset,
covering:
- Missing Value Detection & Visualization
- Outlier Detection & Treatment
- Feature Scaling & Normalization
- Feature Encoding
- Statistical Analysis

---

## 🛠 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Missingno
- Jupyter Notebook

---

## 📊 Topics Practiced

### ✅ Dataset Overview
- Loaded and explored the Employee dataset
- Checked shape, structure, data types
- Identified missing values and basic statistics

### ✅ Missing Value Visualization
Three visualization techniques practiced:
- **Bar Chart** — shows completeness of each column
- **Matrix Plot** — shows missing value patterns across rows
- **Heatmap** — highlights missing locations using coolwarm and viridis colormaps

### ✅ Missing Value Treatment

| Column | Strategy Used |
|--------|--------------|
| Age | Filled with Mean |
| Gender | Filled with Mode |
| Salary | Filled with Mean |

Also practiced using **Scikit-learn SimpleImputer** with:
- Median strategy for Age
- Mean strategy for Salary
- Most Frequent strategy for Gender

### ✅ Outlier Detection
Multiple methods used to detect outliers:

**1. IQR Method (Interquartile Range)**
- Calculated lower and upper bounds using Q1 and Q3
- Identified Row 6 (Grace, Age=120) as outlier

**2. Z-Score Method**
- Used SciPy zscore function
- Threshold adjusted between 2.5 to 3.0 based on dataset size
- Grace (Age=120) detected as outlier

**3. Isolation Forest**
- Machine learning based outlier detection
- contamination parameter set to 0.1
- Output: -1 represents outlier rows, +1 represents normal rows

**4. Boxplot Visualization**
- Vertical boxplot for visual outlier inspection
- Horizontal boxplot for alternative view

### ✅ Outlier Treatment

**Method 1 — Winsorization using SciPy**
- Applied 5% limits on both tails
- Extreme values replaced with boundary values

**Method 2 — Clipping without library**
- Used quantile-based lower and upper bounds
- Age values clipped between 29.5 and 40.0

### ✅ Feature Transformation

**Log Transformation**
- Applied NumPy log to reduce skewness
- Compresses large values effectively

**Power Transformation — Yeo-Johnson**
- Works with both positive and negative values
- Makes data more Gaussian-like

**Power Transformation — Box-Cox**
- Works only with positive values
- Applied using both Scikit-learn and SciPy

### ✅ Feature Scaling

**Standard Scaler (Standardization)**
- Scales values to mean=0 and standard deviation=1
- Output range approximately -1 to +1
- Best for most Machine Learning algorithms

**Min-Max Scaler (Normalization)**
- Scales values strictly between 0 and 1
- Useful when algorithm requires bounded input

### ✅ Feature Encoding

**Label Encoding**
- Converts categories to numeric labels
- F becomes 0, M becomes 1
- Suitable for binary or ordinal categories

**One-Hot Encoding (Dense)**
- Creates separate binary column for each category
- sparse_output=False returns easy-to-read array
- Suitable for nominal categories

**One-Hot Encoding (Sparse)**
- Returns sparse matrix format
- Memory efficient for large datasets
- Stores only non-zero values

**Pandas Get Dummies**
- Quick one-hot encoding using Pandas
- drop_first=True avoids multicollinearity
- Returns True/False boolean columns

**Ordinal Encoding**
- Assigns ordered numeric values to categories
- Suitable when category order matters

---

## 📁 Dataset Description

| Column | Type | Description |
|--------|------|-------------|
| Name | Object | Employee name |
| Age | Float | Employee age — had missing and outlier values |
| Gender | Object | Employee gender — had missing value |
| Salary | Float | Employee salary — had missing value |
| Department | Object | Department name |

**Missing Values Found:**
- Age — 1 missing value
- Gender — 1 missing value
- Salary — 1 missing value

**Outlier Found:**
- Row 6 (Grace) — Age = 120
- Detected by IQR, Z-Score, and Isolation Forest

---

## 🔍 Key Observations

| Observation | Detail |
|-------------|--------|
| Dataset Size | 10 rows × 5 columns |
| Missing Values | 1 each in Age, Gender, Salary |
| Outlier Detected | Grace — Age = 120 |
| Age After Clipping | Capped between 29.5 and 40.0 |
| Best Encoding for Binary | Label Encoding or Get Dummies |
| Best Scaling for ML | StandardScaler |
| Best for Skewed Data | Log or Box-Cox Transformation |

---

## 📈 Learning Outcome

Through this practice, I learned:
- How to identify and visualize missing values using missingno and seaborn
- How to impute missing values using mean, median, and mode strategies
- How to detect outliers using IQR, Z-Score, and Isolation Forest
- How to treat outliers using Winsorization and Clipping
- How to reduce skewness using Log, Box-Cox, and Yeo-Johnson transformations
- How to scale features using StandardScaler and MinMaxScaler
- How to encode categorical variables using multiple encoding strategies
- Differences between Label Encoding, One-Hot Encoding, and Ordinal Encoding

---

## 🎯 Internship Progress

This is **Day 3** of my AI and Machine Learning journey.
I will continue uploading my daily learning progress,
projects, and experiments throughout the internship.

---

## ⭐ Connect With Me

Feel free to explore the repository and follow my learning journey.
