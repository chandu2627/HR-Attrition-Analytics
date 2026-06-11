# 📊 HR Attrition Analytics Dashboard

> **Identifying why employees leave — and what HR can do about it**

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-DAX%20%7C%20Data%20Modeling-yellow?logo=powerbi)
![Dataset](https://img.shields.io/badge/Dataset-IBM%20HR%20Analytics-lightgrey)
![Records](https://img.shields.io/badge/Records-1%2C470%20Employees-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 🧩 Business Problem

High employee attrition is expensive — replacing one employee can cost 50–200% of their annual salary. This project answers three questions HR teams ask every quarter:

- **Who** is leaving — which departments, age groups, and salary bands have the highest risk?
- **Why** are they leaving — what factors (work-life balance, overtime, tenure) drive attrition?
- **What can be done** — which employee segments should HR prioritize for retention?

---

## 🔍 Key Findings

| Metric | Value |
|---|---|
| Overall attrition rate | **16.12%** |
| Highest attrition department | **Sales — 20.6%** |
| Highest attrition age group | **18–25 years — 34.8%** |
| Low salary vs high salary attrition gap | **38% higher** for low salary |
| Poor work-life balance attrition rate | **31.2%** |
| First-year employee attrition | **59 employees left in Year 0–1** |

---

## 🛠️ Tools & Tech Stack

| Layer | Tools Used |
|---|---|
| Data Cleaning & EDA | Python — Pandas, Matplotlib, Seaborn |
| Dashboard & Visualization | Power BI — DAX measures, Data Modeling |
| Data Source | IBM HR Analytics Employee Attrition Dataset (Kaggle) |

---

## 📁 Project Structure

```
HR-Attrition-Analytics/
│
├── HR_Attrition_EDA.ipynb         # Python EDA — cleaning, analysis, 7 visualizations
├── HR_Attrition_Clean.csv         # Cleaned dataset (ready for Power BI)
├── WA_Fn-UseC_-HR-Employee-Attrition.csv  # Original IBM dataset
├── HR_Attrition_Dashboard.pbix    # Power BI dashboard file
├── HR_Attrition_Dashboard.pdf     # Dashboard PDF (preview without Power BI)
└── README.md
```

---

## 📈 Dashboard Pages

### Page 1 — HR Attrition Overview
High-level KPIs: overall attrition rate, headcount, active employees, and attrition breakdown by department, gender, and age band.

### Page 2 — Attrition Drivers
Deep-dive into root causes: salary band, work-life balance score, overtime, job satisfaction, and tenure buckets — with DAX-calculated attrition rates per segment.

> 📄 Can't open .pbix? View the [Dashboard PDF](HR_Attrition_Dashboard.pdf) directly in your browser.

---

## ⚙️ DAX Measures Used

```dax
Attrition Rate = DIVIDE(COUNTROWS(FILTER('HR_Data', 'HR_Data'[Attrition] = "Yes")), COUNTROWS('HR_Data'))

Active Employees = COUNTROWS(FILTER('HR_Data', 'HR_Data'[Attrition] = "No"))

Avg Monthly Income = AVERAGE('HR_Data'[MonthlyIncome])
```

---

## 🚀 How to Run

1. Clone the repo: `git clone https://github.com/chandu2627/HR-Attrition-Analytics.git`
2. Open `HR_Attrition_EDA.ipynb` in Jupyter Notebook
3. Open `HR_Attrition_Dashboard.pbix` in Power BI Desktop
4. Data source is already connected to `HR_Attrition_Clean.csv`

---

## 👤 About

**Polnati Chandu Manikanta Narasimha**
Data Analyst | Power BI · DAX · SQL · Python
📍 Hyderabad, India | Immediate Joiner

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/chandumanikanta)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/chandu2627)

---

*Dataset: IBM HR Analytics Employee Attrition — available on [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)*
