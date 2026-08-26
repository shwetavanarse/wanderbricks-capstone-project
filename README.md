# 🏡 WanderBricks Capstone Project
### End-to-End Data Exploration & Analytics using Databricks, SQL, and GitHub

![Databricks](https://img.shields.io/badge/Platform-Databricks-red?style=for-the-badge&logo=databricks)
![SQL](https://img.shields.io/badge/Language-SQL-blue?style=for-the-badge&logo=mysql)
![GitHub](https://img.shields.io/badge/Version%20Control-GitHub-black?style=for-the-badge&logo=github)
![Status](https://img.shields.io/badge/Project-In%20Progress-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

# 📖 Project Overview

The **WanderBricks Capstone Project** is a comprehensive data analytics project built on the **Databricks Lakehouse Platform**. The objective is to explore, analyze, and derive actionable insights from the WanderBricks travel marketplace dataset.

The project demonstrates an end-to-end analytics workflow including:

- Data Exploration
- Data Quality Assessment
- SQL-based Analysis
- Business Insight Generation
- Exploratory Data Analysis (EDA)
- GitHub Version Control
- Documentation of Findings

This repository serves as a portfolio-ready analytics project showcasing practical SQL and Databricks skills.

---

# 🎯 Project Objectives

The primary objectives of this project are to:

- Explore all available WanderBricks datasets.
- Understand dataset relationships.
- Perform exploratory data analysis.
- Identify missing values and data quality issues.
- Analyze user behavior.
- Generate business insights using SQL.
- Build reusable SQL notebooks.
- Maintain version control using GitHub.

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|----------|
| Databricks | Data Processing & SQL Workspace |
| SQL | Data Exploration & Analytics |
| GitHub | Version Control |
| Delta Lake | Data Storage |
| Markdown | Documentation |

---

# 📂 Repository Structure

```
wanderbricks-capstone/
│
├── README.md
│
├── notebooks/
│   ├── 01_Data_Exploration.sql
│   ├── 02_Users_Analysis.sql
│   ├── 03_Listings_Analysis.sql
│   ├── 04_Bookings_Analysis.sql
│   ├── 05_Reviews_Analysis.sql
│   ├── 06_Payments_Analysis.sql
│   └── 07_Business_Insights.sql
│
├── images/
│
├── docs/
│
└── .gitignore
```

---

# 📊 Dataset

Database Used

```sql
USE samples.wanderbricks;
```

Current exploration focuses on:

- Users
- Listings *(Upcoming)*
- Bookings *(Upcoming)*
- Reviews *(Upcoming)*
- Payments *(Upcoming)*

---

# 📌 Current Analysis

## Users Table

The Users table contains demographic and account information for WanderBricks users.

### Analysis Performed

✔ Data Preview

```sql
SELECT *
FROM users
LIMIT 10;
```

---

✔ Schema Inspection

```sql
DESCRIBE users;
```

---

✔ Total Users

```sql
SELECT
COUNT(*) AS total_rows,
COUNT(DISTINCT user_id) AS unique_users
FROM users;
```

---

✔ User Distribution by Country

```sql
SELECT
country,
COUNT(*) AS total_users
FROM users
GROUP BY country
ORDER BY total_users DESC;
```

---

✔ User Distribution by Type

```sql
SELECT
user_type,
COUNT(*) AS total_users
FROM users
GROUP BY user_type;
```

---

✔ Missing Value Analysis

```sql
SELECT *
FROM users
WHERE
user_type IS NULL
OR country IS NULL
OR email IS NULL
OR company_name IS NULL;
```

---

✔ User Composition

```sql
SELECT
country,
user_type,
COUNT(*)
FROM users
GROUP BY country,user_type;
```

---

✔ Signup Timeline

```sql
SELECT
MIN(created_at),
MAX(created_at)
FROM users;
```

---

✔ Monthly User Growth

```sql
SELECT
YEAR(created_at),
MONTH(created_at),
COUNT(*)
FROM users
GROUP BY
YEAR(created_at),
MONTH(created_at);
```

---

# 🔍 Key Findings

### Users Table

- Contains **100,000 unique users**
- Each row represents one user.
- Supports both **Individual** and **Business** users.
- Missing values observed in:
  - Email
  - Company Name
- User distribution varies significantly across countries.
- Signup activity spans multiple years.
- Monthly trends reveal user acquisition patterns.

---

# 📈 Business Questions Answered

- How many users exist?
- Are there duplicate users?
- Which countries have the highest number of users?
- What is the distribution of business vs individual users?
- Are there missing values?
- When did users join the platform?
- What are the monthly signup trends?

---

# 📋 Data Quality Checks

✔ Duplicate Users

✔ Null Value Detection

✔ Schema Validation

✔ User Type Validation

✔ Country Distribution

✔ Date Validation

---

# 🚀 Future Enhancements

The project will be extended with:

- Listings Analysis
- Booking Trends
- Revenue Analysis
- Customer Segmentation
- Host Performance
- Review Analytics
- Payment Insights
- Cancellation Analysis
- Occupancy Rate Analysis
- Dashboard Development
- Power BI Integration
- Machine Learning Models

---

# 📊 Expected Deliverables

- SQL Exploratory Notebook
- Data Quality Report
- Business Insight Report
- Dashboard
- Documentation
- GitHub Repository

---

# 📚 Learning Outcomes

This project demonstrates:

- SQL Query Writing
- Aggregations
- Filtering
- Grouping
- Sorting
- Date Functions
- Null Handling
- Exploratory Data Analysis
- Data Validation
- Business Analytics
- Databricks Workflow
- Git Version Control

---

# 💡 Skills Demonstrated

- SQL
- Databricks SQL
- Data Exploration
- Data Cleaning
- Analytical Thinking
- Business Intelligence
- GitHub
- Documentation

---

# 👨‍💻 Author

**Shweta Vanarse**

Data Analytics Enthusiast

GitHub: https://github.com/<your-github-username>

LinkedIn: https://linkedin.com/in/<your-linkedin>

---

# ⭐ Repository Status

🚧 **Currently Under Development**

Upcoming modules include advanced SQL analytics, dashboard creation, and end-to-end business intelligence reporting using the WanderBricks dataset.

---

## 🌟 If you found this project helpful, consider giving it a **star** on GitHub!
