# Water-Quality-Potability-Prediction
# 🚀 Day 5 — AI Internship Journey

## 📌 Project Overview
This repository contains my Day 5 learning progress during my AI Internship.
I explored:
- Real-world Water Quality Dataset (fetched from **Snowflake Cloud Database**)
- Missing Value Imputation
- Outlier Detection & Treatment
- Feature Engineering with Log Transformation
- Machine Learning Classification using **Support Vector Machine (SVM)**

Dataset used:
- Water Potability Dataset (`WATER` table from Snowflake — `DB1.PUBLIC.WATER`)

---

# 🛠 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Snowflake Connector
- Google Colab

---

# 📊 Topics Practiced

## ✅ Data Collection
- Connected to **Snowflake Cloud Data Warehouse** using `snowflake.connector`
- Fetched water quality data using SQL query
- Loaded data into a Pandas DataFrame

## ✅ Data Handling & Cleaning
- Checked dataset shape, structure, data types
- Identified and handled missing values using `SimpleImputer` (mean strategy)
- Columns imputed: `PH`, `SULFATE`, `TRIHALOMETHANES`
- Removed duplicate records

## ✅ Outlier Treatment
- Detected outliers using **Boxplots**
- Applied **Winsorization** (5% on both tails) using `scipy.stats.mstats.winsorize`
- Applied **Log Transformation** (`np.log1p`) for normalization

## ✅ Exploratory Data Analysis (EDA)
- Boxplots for all original features
- Scatter plots for feature relationships
- Boxplots for log-transformed features
- Correlation heatmap via Confusion Matrix visualization

## ✅ Machine Learning
- **Model**: Support Vector Classifier (SVC) with Linear Kernel
- **Train-Test Split**: 80% train / 20% test (`random_state=42`)
- **Target Variable**: `POTABILITY` (0 = Not Potable, 1 = Potable)
- **Evaluation Metrics**:
  - Accuracy Score
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)

## ✅ Visualization Techniques
### Matplotlib
- Bar Chart (Actual vs Predicted values)
- Scatter Plots (Feature relationships)
### Seaborn
- Boxplots (Outlier detection)
- Heatmap (Confusion Matrix with annotations)

---

# 📈 Learning Outcome
Through this project, I learned:
- How to connect and fetch data from **Snowflake** cloud data warehouse using Python
- How to handle real-world missing data using `SimpleImputer`
- How to detect and treat outliers using **Winsorization** and **Log Transformation**
- How to build and evaluate an **SVM classification model**
- How to interpret a **Confusion Matrix** and **Classification Report**
- How to visualize actual vs predicted results

---

# 📂 Files Included

| File | Description |
|------|-------------|
| `Water_Quality_Day5.ipynb` | Google Colab notebook |
| `README.md` | Project documentation |

> 📌 Dataset is fetched directly from **Snowflake Cloud** (`DB1.PUBLIC.WATER`) — no local CSV file needed.

---

# 🔍 Key Features in Dataset

| Feature | Description |
|---------|-------------|
| `PH` | pH level of water |
| `HARDNESS` | Calcium & magnesium concentration |
| `SOLIDS` | Total dissolved solids (ppm) |
| `CHLORAMINES` | Chloramines concentration (ppm) |
| `SULFATE` | Sulfate concentration (mg/L) |
| `CONDUCTIVITY` | Electrical conductivity (μS/cm) |
| `ORGANIC_CARBON` | Organic carbon content (ppm) |
| `TRIHALOMETHANES` | Trihalomethanes concentration (μg/L) |
| `TURBIDITY` | Turbidity level (NTU) |
| `POTABILITY` | Target — 1: Potable, 0: Not Potable |

---

# 🎯 Internship Progress
This is **Day 5** of my AI & Machine Learning journey.
I will continue uploading my daily learning progress, projects, and experiments throughout the internship.

---

# ⭐ Connect With Me
Feel free to explore the repository and follow my learning journey.
