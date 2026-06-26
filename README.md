<div align="center">

# 📣 Campaign Performance Prediction

**End-to-end Machine Learning & Analytics project for DOOH Advertising**

*Predicting ROI · Classifying Campaign Success · Visualizing Business Intelligence*

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

</div>

---

## 📌 Project Overview

This project was built during my internship at **Lemma Technologies**, a DOOH (Digital Out-of-Home) advertising company. The goal was to analyze advertising campaign data, predict ROI using regression, classify campaign success using Random Forest, and surface insights through an interactive Power BI dashboard.

The project covers the **full data science pipeline** — from raw data exploration all the way to a business-ready dashboard used by the team.

---

## 📊 Dashboard Preview

### Executive Business Overview
![DOOH Dashboard Overview](assets/dashboard_overview.png)

> 6 KPIs tracked: ₹7.42M Revenue · ₹5.33M Ad Spend · 42.24 Avg ROI · 27M Impressions · 8M Clicks · 30.82% CTR — filterable by ScreenType, Industry, Time Slot, and Weather Condition.

### Campaign Intelligence & Optimization
![Campaign Intelligence](assets/campaign_intelligence.png)

> CTR vs ROI scatter by industry · Revenue treemap by ScreenType · Decomposition tree for weather/time analysis · Top revenue-generating clients (Ola, Netflix, OnePlus, Zomato).

---

## 🗂️ Repository Structure

```
Campaign-Performance-Prediction/
│
├── _EDA Lemma.ipynb                        # Exploratory Data Analysis
├── Campaign Performance Prediction.ipynb   # Classification model (Random Forest)
├── Regression Model to predict ROI.ipynb   # Regression model (Linear + RF)
├── Insights.ipynb                          # Business insights & findings
├── Execute Business Overview.pbix          # Power BI dashboard file
|── dashboard_overview.png
|── campaign_intelligence.png
└── README.md
```

---

## 🔬 Project Workflow

### 1. 📁 Exploratory Data Analysis — `_EDA Lemma.ipynb`
- Distribution analysis of revenue, impressions, clicks, CTR, and ROI
- Industry-wise and screen-type-wise breakdowns
- Correlation heatmaps and outlier detection
- Time slot and weather condition impact on performance

### 2. 🤖 Campaign Performance Classification — `Campaign Performance Prediction.ipynb`
- Binary classification: **High vs Low** performing campaigns
- Feature engineering on CTR, ROI, and Ad Spend
- **Random Forest Classifier** — outperformed Logistic Regression on non-linear patterns
- Evaluation: Accuracy, Precision, Recall, F1-Score, ROC-AUC
- Feature importance analysis to identify top campaign drivers

### 3. 📈 ROI Regression Model — `Regression Model to predict ROI.ipynb`
- Predicting campaign ROI from input features
- Compared **Linear Regression** vs **Random Forest Regressor**
- Metrics: R², MAE, RMSE
- Residual analysis and prediction vs actual plots

### 4. 💡 Business Insights — `Insights.ipynb`
- Industry-level ROI benchmarks (Entertainment & Food top performers at ROI ~44–45)
- Evening time slots drive the highest revenue (₹2.7M vs ₹0.7M at night)
- Revenue nearly evenly distributed across all 5 screen types (~20% each)
- Top clients: Ola, Netflix, OnePlus, Zomato, Samsung, Flipkart

### 5. 📊 Power BI Dashboard — `Execute Business Overview.pbix`
- 2-page interactive dashboard
- Cross-page slicers: ScreenType, Industry, Time Slot, Weather Condition
- Treemap, donut chart, scatter plot, bar charts, decomposition tree
- Designed for executive-level decision making

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.x |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn (Random Forest, Linear Regression, Logistic Regression) |
| BI Dashboard | Microsoft Power BI |
| Notebook Environment | Jupyter Notebook |

---

## 📐 Key Results

| Model | Task | Metric | Result |
|-------|------|--------|--------|
| Random Forest Classifier | Campaign Success Prediction | ROC-AUC | Strong separation |
| Linear Regression | ROI Prediction | R² | Baseline established |
| Random Forest Regressor | ROI Prediction | R² / RMSE | Improved over linear |

> *Exact metric values are documented inside the respective notebooks.*

---

## 💼 Context

This project was developed as part of my role as a **Technical Intern at Lemma Technologies** (May 2026 – Present). Lemma is a DOOH advertising platform, and this analysis directly supported campaign optimization decisions by the business team.

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/prathmesh0work/Campaign-Performance-Prediction.git
cd Campaign-Performance-Prediction

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 3. Run notebooks in this order
#    _EDA Lemma.ipynb  →  Campaign Performance Prediction.ipynb
#    →  Regression Model to predict ROI.ipynb  →  Insights.ipynb

jupyter notebook
```

For the Power BI dashboard, open `Execute Business Overview.pbix` in **Microsoft Power BI Desktop**.

---

## 👤 Author

**Prathmesh Ingole**
Data Analyst Intern @ Lemma Technologies · Pursuing M.Sc. Data Science

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/Prathmesh%20Ingole)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/prathmesh0work)

---

<div align="center">

*Built with real internship data · Designed for business impact · Owned end to end.*

</div>
