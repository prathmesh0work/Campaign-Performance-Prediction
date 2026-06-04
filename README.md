# 📊 DOOH Campaign Analytics & Performance Intelligence

> An end-to-end data science project analyzing **Digital Out-of-Home (DOOH)** advertising campaigns using the Lemma industry-grade dataset — covering exploratory analysis, business insights, ROI prediction, and campaign performance classification.

---

## 🗂️ Project Structure

```
📁 Campaign-Performance-Prediction/
│
├── 📓 _EDA_Lemma.ipynb                        # Exploratory Data Analysis
├── 📓 Insights.ipynb                           # Business Insights & Revenue Analysis
├── 📓 Regression_Model_to_predict_ROI.ipynb    # Linear Regression — ROI Prediction
├── 📓 Campaign_Performance_Prediction.ipynb    # Random Forest — Performance Classification
└── 📊 Execute_Business_Overview.pbix           # Power BI Dashboard
```

---

## 📌 Project Overview

This project explores the **Lemma Industry-Grade DOOH Dataset** (1,000 rows × 28 columns) to uncover patterns in advertising performance and build predictive models for smarter campaign decisions.

The analysis is split across four notebooks, each tackling a distinct layer of the problem:

| Notebook | Purpose |
|---|---|
| `_EDA_Lemma.ipynb` | Data quality checks, shape, types, missing values, duplicates |
| `Insights.ipynb` | Revenue, ROI, and engagement analysis by time slot, weather, and screen |
| `Regression_Model_to_predict_ROI.ipynb` | Predict ROI % using Linear Regression |
| `Campaign_Performance_Prediction.ipynb` | Classify campaign performance using Random Forest |

---

## 📂 Notebook Breakdown

### 1. 🔍 Exploratory Data Analysis — `_EDA_Lemma.ipynb`

Basic health checks and understanding of the dataset before any modeling.

- Dataset shape: **1,000 rows, 28 columns**
- Data type inspection (numeric vs. categorical features)
- Missing value check — ✅ **No null values found**
- Duplicate check — ✅ **No duplicate records found**
- No data cleaning required; dataset is ready for analysis

---

### 2. 💡 Business Insights — `Insights.ipynb`

Deep-dive into revenue, ROI, and audience engagement across different conditions.

**Revenue Analysis**
- Revenue grouped by `time_slot` → **Evening slot drives maximum revenue**
- Revenue grouped by `weather_condition` → **Sunny weather yields highest revenue**
- Top 10 campaigns by total revenue (bar chart visualization)

**ROI Analysis**
- ROI by time slot → **Morning sessions deliver the best average ROI**
- ROI by weather → **Foggy weather surprisingly returns the highest ROI**; Cloudy performs the worst
- ROI distribution histogram

**Audience Engagement**
- Click-Through Rate (CTR) across time slots
- Correlation between `adjusted_impressions` and `revenue`
- Correlation heatmap across 8 key numeric features:
  `impressions`, `adjusted_impressions`, `cpm`, `revenue`, `ad_spend`, `roi_percent`, `click_through_rate`, `estimated_clicks`

**Advanced Insights**
- Best `weather_condition` + `time_slot` combination for maximum revenue
- Top 10 screens by average ROI (`screen_id`)
- CPM efficiency across time slots

---

### 3. 📈 ROI Prediction Model — `Regression_Model_to_predict_ROI.ipynb`

Predicts continuous ROI percentage using **Linear Regression**.

**Features Used**
```
CTR, Spend_INR, Impressions, Clicks, Duration_days,
RunningTime_Hours, ScreenTime_HoursPerDay, cpm, revenue
```

**Pipeline**
1. Train/test split (80/20, `random_state=42`)
2. Feature scaling with `StandardScaler`
3. Linear Regression training
4. Evaluation: **MAE**, **RMSE**, **R² Score**
5. Actual vs. Predicted ROI scatter plot
6. Feature coefficient importance table

---

### 4. 🏆 Campaign Performance Classifier — `Campaign_Performance_Prediction.ipynb`

Classifies `campaign_performance` (target) using **Random Forest**.

**Pipeline**
1. Drop target column → define `X` and `y`
2. Encode all categorical features with `LabelEncoder`
3. Train/test split (80/20, `random_state=42`)
4. Train `RandomForestClassifier` with 100 estimators
5. Evaluation: **Accuracy Score**, **Classification Report**, **Confusion Matrix** heatmap
6. Feature importance bar chart (top 10 features)

---

## 📊 Power BI Dashboard — `Execute_Business_Overview.pbix`

An interactive business overview dashboard built in **Power BI** covering campaign KPIs, revenue trends, and performance summaries for executive-level reporting.

> Open with **Microsoft Power BI Desktop** to explore the interactive visuals.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core language |
| Pandas | Data manipulation |
| Scikit-learn | ML models (Linear Regression, Random Forest, LabelEncoder, StandardScaler) |
| Matplotlib | Visualizations |
| Seaborn | Heatmaps & statistical plots |
| Power BI | Business intelligence dashboard |
| Jupyter Notebook | Interactive analysis environment |

---

## 📦 Installation & Setup

**1. Clone the repository**
```bash
git clone https://github.com/prathmesh0work/Campaign-Performance-Prediction.git
cd Campaign-Performance-Prediction
```

**2. Install dependencies**
```bash
pip install pandas scikit-learn matplotlib seaborn jupyter
```

**3. Add the dataset**

Download the `lemma_industry_grade_doooh_dataset.csv` file and place it in the project root (or update the file path in each notebook accordingly).

**4. Launch Jupyter**
```bash
jupyter notebook
```

---

## 📁 Dataset

- **Name:** Lemma Industry-Grade DOOH Dataset
- **Rows:** 1,000
- **Columns:** 28
- **Key Features:** `impressions`, `adjusted_impressions`, `cpm`, `revenue`, `ad_spend`, `roi_percent`, `click_through_rate`, `estimated_clicks`, `time_slot`, `weather_condition`, `screen_id`, `CampaignID`, `campaign_performance`

> **Note:** Update the CSV path in each notebook from the local Windows path to your own environment path before running.

---

## 📈 Key Findings

- 🌆 **Evening + Sunny** is the highest-revenue combination for DOOH placements
- 🌅 **Morning slots** deliver the best average ROI
- 🌫️ **Foggy weather** unexpectedly produces strong ROI returns
- 📺 Screen selection matters — top 10 screens by ROI significantly outperform the average
- 🌳 **Random Forest** effectively classifies campaign performance with strong accuracy
- 📉 **Linear Regression** provides a solid baseline for ROI prediction

---

## 👤 Author

**Prathmesh Ingole** — [@prathmesh0work](https://github.com/prathmesh0work)

---

## 📄 License

This project is for educational and analytical purposes. Dataset credits to **Lemma Technologies**.
