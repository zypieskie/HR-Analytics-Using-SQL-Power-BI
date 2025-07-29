# HR Analytics Using SQL & Power BI

This project explores an HR dataset to analyze employee demographics, trends, and termination patterns using SQL for data transformation and Power BI for interactive visualization.

## 📊 Project Overview

The aim of this project is to gain insights into workforce characteristics such as:
- Employee distribution by age, gender, department, and race
- Termination rates across departments
- Change in employee numbers over time
- Average employee tenure
- Office vs. remote workforce trends

## 🗂 Dataset

- **Source:** [HR Dataset on Kaggle](https://www.kaggle.com/datasets/priykushwaha/hr-dataset)
- **Content:** The dataset includes information such as:
  - `id`, `name`, `birthdate`, `hire_date`, `termdate`
  - `gender`, `race`, `location`, `state`
  - `department`, `position`, `employee_status`

## 🛠 Tools & Technologies

- **SQL (MySQL)** – for data cleaning, transformation, and age calculation
- **Power BI** – for data visualization and interactive dashboard creation
- **Excel/CSV** – dataset formatting
- **Kaggle** – dataset source

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
- ![Dashboard Page 1](./screenshots/Screenshot_1.png)
- ![Dashboard Page 2](./screenshots/Screenshot_2.png)

> *Note: Ensure these screenshot files (`Screenshot_1.png`, `Screenshot_2.png`) are placed in a `/screenshots` folder within your GitHub repo.*

## 📂 Folder Structure (Suggested)

```
HR-Analytics-SQL-PowerBI/
├── README.md
├── sql/
│   └── hr_analysis_queries.sql
├── powerbi/
│   └── HR_Analytics_Report.pbix
├── data/
│   └── HRDataset.csv
└── screenshots/
    ├── Screenshot_1.png
    └── Screenshot_2.png
```

## 📌 Key Findings

- Most employees are aged between 25–54 years
- Majority of workforce is male (8.9K) and based at headquarters (13K)
- Highest employee concentration in Ohio, Pennsylvania, and Illinois
- Departments like Auditing and Legal have relatively higher termination rates

## ✅ Conclusion

This project demonstrates how SQL and Power BI can be used together to uncover meaningful HR trends and support data-driven workforce decisions.

## 🔗 Links

- 📂 [Power BI Report](https://umsedumy-my.sharepoint.com/:u:/g/personal/muhammad_hanafi_bi21_iluv_ums_edu_my/EdVMTx1MoVVJsR7fRrAnxsYBfise1X3ia2cEYmGwuGLg0Q?e=5oUXri)
- 🧠 [SQL Script](Add SQL GitHub link if hosted)
- 📊 [Dataset on Kaggle](https://www.kaggle.com/datasets/priykushwaha/hr-dataset)
