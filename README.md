# 📊 Excelrate Data Visualization & Analytics Internship

> **Role:** Data Visualization Associate Intern  
> **Internship:** Excelrate  
> **Mode:** Remote  
> **Project:** Integrated Opportunity & Learner Analytics Dashboard

---

## 📌 Overview

This repository contains the work completed during my **Data Visualization Associate Internship at Excelrate**.

The project focused on transforming raw organizational datasets into meaningful business insights through **data cleaning, SQL-based analysis, dataset integration, and interactive dashboard development**.

The overall workflow followed an end-to-end data analytics pipeline:

**CSV Files → PostgreSQL → Data Cleaning → SQL Analysis → Dataset Integration → Google Sheets → Looker Studio → Dashboard & Insights**

---

## 🎯 Project Objectives

- Import and manage Opportunity and Learner datasets in PostgreSQL
- Clean and validate raw datasets
- Handle missing and inconsistent data
- Perform SQL-based exploratory and analytical queries
- Integrate learner and opportunity datasets
- Create meaningful KPIs and visualizations
- Develop interactive dashboards using Looker Studio
- Communicate findings through data storytelling

---

## 📂 Datasets

### Opportunity Dataset

The Opportunity dataset contains information related to available opportunities.

**Key fields:**
- Opportunity ID
- Category
- Cohort
- Fee
- Reward
- Duration
- Role
- Location

**Records:** 5,300

### Learner Dataset

The Learner dataset contains information related to learner applications and participation.

**Key fields:**
- Learner Status
- Payment Status
- Category
- Apply Date
- Cohort
- Reward
- Completion Date

**Records:** 15,029

---

## 🛠️ Tools & Technologies

| Category | Tools |
|---|---|
| Database | PostgreSQL |
| Query Language | SQL |
| Data Cleaning | SQL |
| Data Validation | SQL |
| Data Integration | SQL JOINs |
| Spreadsheet | Google Sheets |
| Visualization | Looker Studio, PowerBI |
| Analytics | Exploratory Data Analysis |
| Presentation | Data Storytelling |

---

## 🔄 Project Workflow

```text
Raw CSV Files
     ↓
PostgreSQL
     ↓
Data Cleaning & Validation
     ↓
SQL Analysis
     ↓
Dataset Integration
     ↓
Google Sheets
     ↓
Looker Studio, PowerBI
     ↓
Interactive Dashboard
     ↓
Business Insights
````

---

## 🧹 Data Cleaning & Preparation

The datasets were cleaned and validated before analysis.

### Key operations performed

* Removed duplicate records
* Checked for missing values
* Standardized inconsistent values
* Handled NULL values
* Validated data using aggregate queries
* Prepared datasets for integration and visualization

### Example

```sql
SELECT DISTINCT *
FROM learner_data_raw;
```

Checking missing values:

```sql
SELECT *
FROM learner_data_raw
WHERE status IS NULL;
```

Standardizing missing payment status:

```sql
UPDATE learner_data_raw
SET payment_status = 'Unpaid'
WHERE payment_status IS NULL;
```

---

## 🔎 SQL Analysis

SQL was used extensively to explore the datasets and generate analytical insights.

### Opportunity Category Analysis

```sql
SELECT
    category,
    COUNT(*) AS total
FROM opportunity_data_raw
GROUP BY category
ORDER BY total DESC;
```

### Learner Status Analysis

```sql
SELECT
    status,
    COUNT(*) AS learners
FROM learner_data_raw
GROUP BY status
ORDER BY learners DESC;
```

### Payment Status Analysis

```sql
SELECT
    payment_status,
    COUNT(*) AS total
FROM learner_data_raw
GROUP BY payment_status;
```

### Cohort Analysis

```sql
SELECT
    cohort,
    COUNT(*) AS learners
FROM learner_data_raw
GROUP BY cohort
ORDER BY learners DESC;
```

### Average Opportunity Fee

```sql
SELECT AVG(fee)
FROM opportunity_data_raw;
```

### Total Rewards

```sql
SELECT SUM(reward)
FROM opportunity_data_raw;
```

---

## 🔗 Dataset Integration

The Opportunity and Learner datasets were integrated using a SQL `LEFT JOIN` based on the assigned cohort.

```sql
SELECT *
FROM learner_data_raw l
LEFT JOIN opportunity_data_raw o
ON l.assigned_cohort = o.cohort;
```

This integrated dataset was then prepared for reporting and dashboard development.

---

## 📊 Dashboard

An interactive **Opportunity & Learner Analytics Dashboard** was developed using Looker Studio.

### KPI Cards

The dashboard included key metrics such as:

* Total Opportunities
* Total Learners
* Average Fee
* Total Rewards
* Total Applications
* Approved Applications
* Total Fees

### Visualizations

The dashboard included visual analysis such as:

* Applications by Opportunity Category
* Learner Status Distribution
* Payment Status Distribution
* Application Trends
* Learner Distribution by Cohort
* Lead Source Distribution

---

## 💡 Key Insights

The analysis produced several important findings:

1. **Internship opportunities represented the largest opportunity category.**
2. **A few major cohorts accounted for a large share of learner applications.**
3. **Payment completion presented an opportunity for improvement.**
4. **Data cleaning improved the quality and reliability of analysis.**
5. **Interactive dashboards simplified performance monitoring.**

---

## 📈 Recommendations

Based on the analysis, the following recommendations were identified:

* Improve data validation during data entry
* Reduce missing values by introducing mandatory fields
* Automate dashboard refresh processes
* Monitor learner payment status regularly
* Maintain consistent naming conventions across datasets

---

## 🧠 Skills Developed

### Technical Skills

* PostgreSQL
* SQL
* Data Cleaning
* Data Validation
* Data Integration
* Google Sheets
* Looker Studio
* PowerBI
* Dashboard Design
* Data Visualization
* Data Storytelling

### SQL Concepts

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `COUNT()`
* `SUM()`
* `AVG()`
* `CASE`
* `JOIN`
* `DISTINCT`
* Aggregate Functions

### Professional Skills

* Analytical Thinking
* Problem Solving
* Communication
* Team Collaboration
* Presentation Skills

---

## 🚧 Challenges & Solutions

| Challenge               | Solution                             |
| ----------------------- | ------------------------------------ |
| Large datasets          | SQL-based data processing            |
| Missing values          | NULL value handling                  |
| Inconsistent data       | Data standardization                 |
| Dataset integration     | SQL JOIN operations                  |
| Dashboard configuration | Interactive Looker Studio dashboards |

---

## 📁 Repository Structure

```text
Excelrate-Data-Visualization-Internship/
│
├── README.md
│
├── data/
│   ├── opportunity_data.csv
│   └── learner_data.csv
│
├── sql/
│   ├── data_cleaning.sql
│   ├── data_validation.sql
│   ├── data_analysis.sql
│   └── data_integration.sql
│
├── dashboard/
│   └── dashboard_screenshots/
│
├── presentation/
│   └── internship_final_presentation.pdf
│
└── documentation/
    └── project_notes.md
```

> **Note:** Update the repository structure according to the files you actually upload to GitHub.

---

## 🎓 Internship Outcome

This internship provided practical experience in an end-to-end data analytics workflow, from **raw dataset preparation and SQL analysis to dashboard development and business insight generation**.

The project strengthened my ability to:

* Work with real-world datasets
* Clean and validate data
* Perform analytical SQL queries
* Integrate multiple datasets
* Design interactive dashboards
* Extract actionable insights
* Present analytical findings effectively

---

## 👨‍💻 Role

**Data Visualization Associate Intern — Excelrate**

During the internship, I worked on data preparation, SQL analysis, dataset integration, dashboard development, and data storytelling as part of the analytics workflow.

---

## 📌 Project Highlights

* 📊 Analyzed **15,029 learner records**
* 📈 Worked with **5,300 opportunity records**
* 🧹 Performed data cleaning and validation
* 🔎 Conducted SQL-based analysis
* 🔗 Integrated multiple datasets using SQL JOINs
* 📊 Developed interactive analytics dashboards
* 💡 Generated actionable business insights

---

## ⭐ Acknowledgement

This project was completed as part of my **Data Visualization Associate Internship at Excelrate**.

---

**If you found this project useful, feel free to ⭐ star the repository!**

```

### One recommendation for your GitHub

Since you're targeting **Data Analyst / BI Analyst / Data Visualization roles**, I'd name the repository something professional like:

**`excelrate-data-visualization-internship`**

and use this short GitHub description:

> **End-to-end data analytics project involving data cleaning, PostgreSQL, SQL analysis, dataset integration, and interactive Looker Studio dashboards.**

The internship presentation itself confirms the project outcome as **cleaning and analyzing real-world datasets, developing SQL-based analytical solutions, building interactive dashboards, and delivering actionable business insights**. :contentReference[oaicite:2]{index=2}
```
