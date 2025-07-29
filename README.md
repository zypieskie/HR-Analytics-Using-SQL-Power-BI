# HR Analytics Using SQL & Power BI

This project explores an HR dataset to analyze employee demographics, trends, and termination patterns using SQL for data transformation and Power BI for interactive visualization.

## 📊 Project Overview

The aim of this project is to gain insights into workforce characteristics such as:
- Employee distribution by age, gender, department, and race
- Termination rates across departments
- Change in employee numbers over time
- Average employee tenure
- Office vs. remote workforce trends

---

## 🗂 Dataset

- **Source:** [HR Dataset on Kaggle](https://www.kaggle.com/datasets/priykushwaha/hr-dataset)
- **Content:** The dataset includes information such as:
  - `id`, `name`, `birthdate`, `hire_date`, `termdate`
  - `gender`, `race`, `location`, `state`
  - `department`, `position`, `employee_status`
 
---

## 🛠 Tools & Technologies

- **SQL (MySQL)** – for data cleaning, transformation, and age calculation
- **Power BI** – for data visualization and interactive dashboard creation
- **Excel/CSV** – dataset formatting
- **Kaggle** – dataset source

---

## 🧹 Data Cleaning in SQL

Key transformations:
- Cleaned inconsistent date formats using `STR_TO_DATE` and `DATE_FORMAT`
- Converted string-formatted dates into valid `DATE` types (`birthdate`, `hire_date`, `termdate`)
- Handled invalid termination dates (`0000-00-00`)
- Added `age` column using `TIMESTAMPDIFF(YEAR, birthdate, CURDATE())`

Example SQL snippet:
```sql
ALTER TABLE hr
MODIFY COLUMN birthdate DATE;

UPDATE hr
SET age = TIMESTAMPDIFF(YEAR, birthdate, CURDATE());
```

---

## 📈 Power BI Dashboard

### Key Insights Visualized:
- **Gender Distribution**: Male vs. Female vs. Non-Conforming
- **Employee Location**: Headquarters vs. Remote
- **Age Group & Distribution**: Age breakdown by gender
- **Race Distribution**
- **Employee by State**: Using filled map
- **Average Employment Duration**: 8 years
- **Termination Rate by Department**
- **Employee Count Change (2000–2021)**

### Sample Dashboards:
1. **Overview Dashboard** – Shows gender, age group, and location distribution
<img width="1306" height="734" alt="page 1" src="https://github.com/user-attachments/assets/228eeb8c-2080-4ab8-b3f5-9e6be67b30b6" />

2. **Terminations & Trends** – Termination rates, employee growth over time, and tenure by department
<img width="1308" height="734" alt="page 2" src="https://github.com/user-attachments/assets/a9618024-296e-4f18-9235-0c1567ac5960" />

---

## 📌 Key Findings

- Most employees are aged between 25–54 years
- Majority of workforce is male (8.9K) and based at headquarters (13K)
- Ohio leads as the top state for employee concentration, followed by Pennsylvania and Illinois
- Departments such as Auditing (20%), Legal (15%), and Training (13%) have the highest termination rates
- Average employment duration for terminated employees is around 8 years
- Employee retention rates have improved over the years, reaching 95.66% in 2020

---

## ✅ Conclusion

This project demonstrates how SQL and Power BI can be used together to uncover meaningful HR trends and support data-driven workforce decisions.

## 🔗 Links

- 📂 [Power BI Report](https://umsedumy-my.sharepoint.com/:u:/g/personal/muhammad_hanafi_bi21_iluv_ums_edu_my/EdVMTx1MoVVJsR7fRrAnxsYBfise1X3ia2cEYmGwuGLg0Q?e=5oUXri)
- 🧠 [SQL Cleaning](https://github.com/zypieskie/HR-Analytics-Using-SQL-Power-BI/blob/main/HR%20Data%20Cleaning.sql)
- 🧠 [SQL Question](https://github.com/zypieskie/HR-Analytics-Using-SQL-Power-BI/blob/main/HR%20Data%20Questions.sql)
- 📊 [Dataset on Kaggle](https://www.kaggle.com/datasets/priykushwaha/hr-dataset)
