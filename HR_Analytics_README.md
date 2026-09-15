# 👥 HR Employee Analytics Project

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-green?logo=pandas)
![Tableau](https://img.shields.io/badge/Tableau-Dashboard-orange?logo=tableau)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Project Overview

An end-to-end HR data analytics project on a messy employee dataset of 1,020 records.
The project covers the complete data analyst workflow — from raw messy data to an
interactive Tableau dashboard published on Tableau Public.

**Goal:** Clean and analyze employee data to extract actionable HR insights on
department performance, salary distribution, employee status, and regional trends.

---

## 📂 Project Structure

```
HR-Employee-Analytics-Project/
│
├── Messy_Employee_dataset.csv          # Raw messy dataset (original)
├── Messy_Cleaned.csv                   # Cleaned dataset (output)
├── Data_Cleaning.ipynb                 # Python data cleaning notebook
├── Messy_Employee_Data_Dashboard.twb   # Tableau workbook
├── Dashboard_For_Messy_Employee_Project.png  # Dashboard screenshot
└── README.md                           # Project documentation
```

---

## 📊 Dataset Overview

| Property | Details |
|---|---|
| Source | Kaggle — Messy HR Employee Dataset |
| Raw Rows | 1,020 rows |
| Columns | 12 columns (raw) → 17 columns (cleaned) |
| Format | CSV |

### Columns Description

| Column | Description |
|---|---|
| Employee_ID | Unique employee identifier |
| First_Name | Employee first name |
| Last_Name | Employee last name |
| Age | Employee age |
| Department_Region | Combined department and region (e.g., DevOps-California) |
| Status | Employment status — Active, Inactive, Pending |
| Join_Date | Date employee joined the company |
| Salary | Annual salary |
| Email | Employee email address |
| Phone | Employee phone number |
| Performance_Score | Performance rating — Excellent, Good, Average, Poor |
| Remote_Work | Whether employee works remotely |

---

## 🧹 Data Quality Issues Found

The raw dataset had the following issues identified and resolved:

| Issue | Details |
|---|---|
| Missing Values | 235 missing values — Age (211), Salary (24) |
| Invalid Phone Numbers | All phone numbers were negative integers — invalid format |
| Combined Column | Department and Region were merged in one column (e.g., "DevOps-California") |
| No Duplicates | Dataset had no duplicate records |

---

## 🔧 Data Cleaning Steps

All cleaning performed in Python using Pandas — see `Data_Cleaning.ipynb`

1. **Split Department_Region column** — Extracted Department and Region into two separate columns using `str.split('-', expand=True)`

2. **Handled missing Age values** — 211 null values filled using median age grouped by Department to preserve realistic distribution

3. **Handled missing Salary values** — 24 null values filled using median salary grouped by Department

4. **Invalid phone number treatment** — Invalid phone numbers were identified using a 10-digit validation rule. Invalid values were replaced with missing values rather than deleting the employee records, preserving the integrity of the employee dataset.

5. **Email validation** — Validated email format using regex pattern; flagged invalid emails with a new `Email_Status` column

6. **Created Phone_Status column** — Added validation flag to indicate valid/invalid phone records

7. **Standardized date format** — Converted Join_Date to consistent datetime format

---

## 📈 Key Insights from EDA

- **Total Employees:** 1,020 across 6 departments and 6 regions
- **Largest Department:** DevOps (189 employees)
- **Smallest Department:** Cloud Tech (146 employees)
- **Average Salary:** ₹85,164 across all departments
- **Highest Paying Department:** Sales (highest average salary)
- **Top Region by Employees:** California (187 employees)
- **Employee Hiring Trend:** Consistent hiring from 2020 to 2024 with peak in 2023

---

## 📊 Tableau Dashboard

Interactive dashboard published on Tableau Public — see `Messy_Employee_Data_Dashboard.twb`

### Dashboard Visuals

| Visual | Insight |
|---|---|
| Total Employees by Department (Bar Chart) | Headcount distribution across departments |
| Average Salary by Department (Bar Chart) | Salary comparison across departments |
| Employee Status by Department (Stacked Bar) | Active vs Inactive vs Pending by department |
| Performance by Department (Stacked Bar) | Performance score distribution per department |
| Average Salary by Region (Bar Chart) | Regional salary comparison |
| Average Salary by Performance (Bar Chart) | Salary vs performance correlation |
| Employee Joining Over Year (Line Chart) | Hiring trend from 2020 to 2024 |

### Dashboard Preview
![HR Employee Analytics Dashboard](Dashboard_For_Messy_Employee_Project.png)

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| Python 3.x | Data processing |
| Pandas | Data cleaning and manipulation |
| Jupyter Notebook | Interactive development |
| Tableau Desktop | Dashboard creation |
| Tableau Public | Dashboard publishing |
| Git & GitHub | Version control |

---

## 💡 Key Business Insights

1. **DevOps** has the highest headcount but **Sales** has the highest average salary — potential retention risk in DevOps
2. **Cloud Tech** is the smallest department — may indicate scope for expansion
3. **California** leads in employee count — highest operational presence
4. Salary distribution across performance scores shows minimal gap between Good and Excellent — compensation review recommended
5. Consistent hiring trend from 2020–2024 with a peak in 2023 — company growth phase visible

---

## 🚀 How to Run

### Python Notebook:
```bash
# Clone the repository
git clone https://github.com/akshatpandeyofficial/HR-Employee-Analytics-Project

# Install dependencies
pip install pandas numpy jupyter

# Open notebook
jupyter notebook Data_Cleaning.ipynb
```

### Tableau Dashboard:
- Open `Messy_Employee_Data_Dashboard.twb` in Tableau Desktop
- Or view on Tableau Public — [](https://public.tableau.com/views/MessyEmployeeDataDashboard/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 👨‍💻 Author

**Akshat Pandey**
- 📧 akshatpandey.dev@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/akshatpandeyofficial)
- 🐙 [GitHub](https://github.com/akshatpandeyofficial)


