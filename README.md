
# 👥 HR Attrition Analytics
**Workforce Attrition Intelligence Dashboard** — An end-to-end analytics project identifying key employee attrition drivers using Python EDA and Power BI Dashboard.

---

## 📌 Project Overview
This project analyzes **1,470 IBM HR employee records** to uncover attrition patterns, workforce trends, and retention risk factors. The goal is to provide actionable insights for HR teams to reduce employee turnover, improve job satisfaction, and optimize workforce planning.

---

## 🎯 Problem Statement
Organizations often struggle to identify:
- 📉 Which departments and job roles have the highest attrition risk
- 💰 How salary bands and compensation impact employee retention
- 👥 Which age groups and tenure stages are most vulnerable to attrition
- 😊 How job satisfaction and work-life balance influence employee decisions
- ⏰ How overtime affects attrition rates across departments

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Pandas, Matplotlib, Seaborn) | Data cleaning, EDA & visualizations |
| SQL | Data aggregation & KPI calculation |
| Power BI (DAX, Power Query) | Interactive 2-page dashboard |
| Jupyter Notebook | EDA pipeline & insights |

---

## 📊 Dataset

| Field | Details |
|-------|---------|
| Records | 1,470 employee records |
| Fields | Age, Department, JobRole, MonthlyIncome, Attrition, JobSatisfaction, WorkLifeBalance, OverTime, YearsAtCompany, and 26 more |
| Source | IBM HR Analytics Employee Attrition Dataset — Kaggle |
| File | WA_Fn-UseC_-HR-Employee-Attrition.csv |

---

## 🔑 Key Python EDA Insights

### 1. Overall Attrition Rate
```python
attrition_rate = df['Attrition'].value_counts(normalize=True) * 100
# Attrition Rate: 16.12% | Retention Rate: 83.88%
```

### 2. Attrition by Department
```python
dept_attrition = df.groupby('Department')['Attrition'].apply(
    lambda x: (x=='Yes').sum() / len(x) * 100
)
# Sales: 20.6% | Human Resources: 19.0% | R&D: 13.8%
```

### 3. Attrition by Age Group
```python
df['Age_Group'] = pd.cut(df['Age'], bins=[18,25,35,45,60],
                          labels=['18-25','26-35','36-45','46-60'])
# 18-25: 34.8% | 26-35: 19.1% | 36-45: 9.2% | 46-60: 12.5%
```

### 4. Attrition by Monthly Income
```python
# Median Income - Attrition: $3,202
# Median Income - Retained: $5,204
# Low salary employees leave 38% more than high salary employees
```

---

## 💡 Key Insights

- 🏆 **Sales department** has highest attrition at **20.6%**
- 👶 **18-25 age group** has highest attrition rate at **34.8%**
- 💰 Employees who left earned **38% less** than those who stayed
- 😟 **Bad work-life balance** employees have **31.2%** attrition rate
- ⏰ **Year 0-1** employees have highest attrition with **59 employees** leaving
- 👔 **Laboratory Technicians** have the highest attrition by job role
- 😊 **Low job satisfaction** leads to **22.8%** attrition vs **11.3%** for very high satisfaction

---

## 📋 Dashboard Pages

### Page 1 — HR Attrition Overview Dashboard
- 4 KPI Cards: Total Employees, Attrition Count, Attrition Rate %, Avg Monthly Income
- Attrition by Department (Bar Chart)
- Attrition by Age Group (Column Chart)
- Attrition by Gender (Donut Chart)
- Attrition by OverTime (Column Chart)
- Slicers: Age Group, Department, Gender

### Page 2 — HR Attrition Drivers Dashboard
- Attrition by Job Satisfaction
- Attrition by Work Life Balance
- Attrition by Salary Band
- Attrition by Job Role
- Attrition by Years at Company (Line Chart)
- Slicers: Department, Gender, OverTime

---

## 📁 Repository Files

| File | Description |
|------|-------------|
| WA_Fn-UseC_-HR-Employee-Attrition.csv | Raw IBM HR dataset |
| HR_Attrition_EDA.ipynb | Python EDA notebook with 7 visualizations |
| HR_Attrition_Clean.csv | Cleaned dataset with engineered columns |
| HR_Attrition_Dashboard.pdf | Power BI 2-page dashboard export |
| HR_Attrition_Dashboard.pbix | Power BI dashboard file |

---
## 👤 Author
**Chandu Manikanta**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin)](https://www.linkedin.com/in/polnati-chandu-manikanta-narasimha-0b4802259) [![GitHub](https://img.shields.io/badge/GitHub-black?logo=github)](https://github.com/chandu2627)
