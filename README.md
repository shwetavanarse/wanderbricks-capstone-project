# 🏡 WanderBricks — Exploratory Data Analysis

### SQL-Based Travel Marketplace Data Exploration using Databricks

[![Databricks](https://img.shields.io/badge/Databricks-Lakehouse-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://www.databricks.com/)
[![SQL](https://img.shields.io/badge/SQL-Data%20Analysis-336791?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.mysql.com/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/)

> **WanderBricks is a SQL-based Exploratory Data Analysis project built in Databricks to understand the structure, quality, and key characteristics of a travel marketplace dataset across users, properties, hosts, bookings, reviews, and amenities.**

---

## 📌 Project Overview

**WanderBricks** is a travel marketplace analytics project focused on exploring interconnected datasets representing different aspects of a property-booking platform.

The project begins with **Exploratory Data Analysis (EDA)** across multiple business entities to understand:

- 👥 Users
- 🏠 Properties
- 👤 Hosts
- 📅 Bookings
- ⭐ Reviews
- 🛎️ Amenities

The analysis is performed using **SQL within Databricks**, with each business entity explored through a dedicated notebook.

The objective is to understand the available data, identify important patterns, assess data quality, and establish a strong analytical foundation for subsequent business analysis.

---

# 🎯 Project Objectives

The main objectives of this EDA project are to:

- Understand the structure of the WanderBricks data model
- Explore individual business tables
- Examine record counts and distributions
- Identify missing and potentially inconsistent data
- Understand relationships between marketplace entities
- Investigate important categorical and numerical attributes
- Explore booking, property, host, user, review, and amenity data
- Prepare the dataset for deeper business analytics

---

# 🗂️ Data Domains Explored

The project currently contains **six dedicated EDA notebooks**.

| # | Analysis | Business Area |
|---|---|---|
| 01 | 👥 User Table EDA | Customer/User Analytics |
| 02 | 🏠 Properties EDA | Property Marketplace |
| 03 | 👤 Hosts EDA | Host Analytics |
| 04 | 📅 Booking EDA | Booking & Reservation Analytics |
| 05 | ⭐ Reviews EDA | Customer Feedback |
| 06 | 🛎️ Amenities EDA | Property Features |

---

# 🔍 Exploratory Data Analysis

## 👥 01. User Table EDA

The user dataset is explored to understand the platform's customer base.

### Focus Areas

- User records
- User attributes
- User distribution
- User types
- Geographic information
- Data completeness
- Potential duplicate records
- User-related categorical fields

This analysis establishes an understanding of the platform's user population before connecting users with other marketplace activities.

---

## 🏠 02. Properties EDA

The properties dataset represents the accommodation inventory available on the platform.

### Focus Areas

- Property records
- Property attributes
- Property categories
- Location information
- Pricing-related fields
- Property characteristics
- Data completeness
- Distribution of property attributes

This analysis helps understand the supply side of the WanderBricks marketplace.

---

## 👤 03. Hosts EDA

The hosts dataset is explored to understand the individuals or entities providing properties on the platform.

### Focus Areas

- Host records
- Host attributes
- Host characteristics
- Geographic distribution
- Host-related categories
- Data completeness
- Host/property relationships

Host-level exploration provides a foundation for later analysis of host performance and marketplace supply.

---

## 📅 04. Booking EDA

The booking dataset represents reservation activity on the platform.

### Focus Areas

- Booking records
- Booking attributes
- Booking dates
- Reservation-related fields
- Booking status information
- Guest/property relationships
- Data completeness
- Temporal patterns

The booking EDA provides the foundation for understanding marketplace demand and reservation activity.

---

## ⭐ 05. Reviews EDA

The reviews dataset captures customer feedback associated with marketplace activity.

### Focus Areas

- Review records
- Ratings
- Review-related attributes
- Customer/property relationships
- Review distributions
- Data completeness
- Feedback patterns

Review exploration creates a foundation for future customer satisfaction and property-quality analysis.

---

## 🛎️ 06. Amenities EDA

The amenities dataset represents the facilities and features associated with properties.

### Focus Areas

- Amenity records
- Amenity categories
- Property-amenity relationships
- Amenity availability
- Distribution of amenities
- Data completeness

This analysis helps establish how property features are represented within the marketplace dataset.

---

# 🔄 EDA Workflow

```text
                    ┌──────────────────────┐
                    │ WanderBricks Dataset │
                    └───────────┬──────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │   Data Exploration   │
                    └───────────┬──────────┘
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
          ▼                     ▼                     ▼
     👥 Users              🏠 Properties          👤 Hosts
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
          ▼                     ▼                     ▼
      📅 Bookings            ⭐ Reviews            🛎️ Amenities
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │ Data Quality &       │
                    │ Pattern Identification│
                    └───────────┬──────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │ Further Business     │
                    │ Analytics            │
                    └──────────────────────┘
```

---

# 🧠 Analytical Approach

Each dataset is explored independently before being considered in the broader marketplace context.

The general EDA process follows:

### 1️⃣ Understand

Inspect the available tables, columns, and data types.

### 2️⃣ Profile

Examine record counts, distributions, and important attributes.

### 3️⃣ Validate

Look for:

- Missing values
- Duplicate records
- Unexpected values
- Inconsistent categories
- Data-type issues

### 4️⃣ Explore

Use SQL aggregations and filtering to identify patterns and distributions.

### 5️⃣ Connect

Understand how users, hosts, properties, bookings, reviews, and amenities relate to one another.

### 6️⃣ Prepare

Use the findings from EDA as a foundation for deeper business analytics.

---

# 🛠️ Technology Stack

| Technology | Usage |
|---|---|
| **Databricks** | Data exploration and SQL execution |
| **SQL** | EDA, aggregation, filtering and analysis |
| **Jupyter Notebooks** | Organizing analytical queries |
| **GitHub** | Version control and project documentation |
| **Delta/Lakehouse Environment** | Working with structured analytical data |

---

# 📁 Repository Structure

```text
wanderbricks-capstone-project/
│
├── 01_data_exploration/
│   │
│   ├── amenities eda.dbquery.dbquery.ipynb
│   ├── booking eda.dbquery.dbquery.ipynb
│   ├── hosts eda.dbquery.dbquery.ipynb
│   ├── properties eda.dbquery.dbquery.ipynb
│   ├── reviews eda.dbquery.dbquery.ipynb
│   └── user table eda.dbquery.ipynb
│
└── README.md
```

---

# 📊 Project Coverage

The current EDA covers the major entities of a travel marketplace:

```text
                    WANDERBRICKS
                         │
       ┌─────────────────┼─────────────────┐
       │                 │                 │
       ▼                 ▼                 ▼
     USERS            HOSTS           PROPERTIES
       │                 │                 │
       │                 └────────┬────────┘
       │                          │
       └──────────────┬───────────┘
                      ▼
                   BOOKINGS
                      │
              ┌───────┴───────┐
              ▼               ▼
           REVIEWS         AMENITIES
```

This structure allows the project to move beyond isolated table exploration toward **marketplace-level analytics**.

---

# 💡 Business Questions Enabled by the EDA

The exploratory analysis establishes the foundation for answering questions such as:

### 👥 Users
- Who are the users of the platform?
- Where are users located?
- What user categories exist?
- Are there missing or duplicate user records?

### 🏠 Properties
- What types of properties are available?
- Where are properties concentrated?
- What characteristics define the available inventory?

### 👤 Hosts
- How many hosts operate on the platform?
- How are hosts distributed geographically?
- How are hosts connected to properties?

### 📅 Bookings
- How is booking activity distributed?
- What time periods have higher booking activity?
- What booking statuses exist?

### ⭐ Reviews
- How are ratings distributed?
- Which properties receive reviews?
- What patterns exist in customer feedback?

### 🛎️ Amenities
- What amenities are available?
- Which amenities are most common?
- How are amenities associated with properties?

---

# 📈 Why This Project Matters

A travel marketplace contains multiple interconnected sources of information.

Looking at only one table can provide an incomplete picture.

By exploring **users → hosts → properties → bookings → reviews → amenities**, this project establishes the foundation for understanding the complete marketplace ecosystem.

This approach demonstrates how an analyst can move from:

**Raw Data → Data Understanding → Data Quality → Exploration → Business Analysis**

---

# 🚀 Next Analytical Opportunities

The EDA phase creates a strong foundation for more advanced analysis, including:

- 📊 Marketplace performance analysis
- 💰 Revenue and pricing analysis
- 📅 Booking trend analysis
- 🏠 Property performance analysis
- 👤 Host performance analysis
- ⭐ Rating and review analysis
- 🛎️ Amenity impact analysis
- 👥 Customer segmentation
- 🌍 Geographic market analysis
- 📈 KPI development
- 📊 Business intelligence dashboards

---

# 🎓 Skills Demonstrated

### SQL & Data Analysis

- Data exploration
- Filtering
- Aggregation
- Grouping
- Sorting
- Data profiling
- NULL/missing-value analysis
- Categorical analysis
- Date-based exploration
- Relational data understanding

### Analytics

- Exploratory Data Analysis
- Data quality assessment
- Business question formulation
- Marketplace analysis
- Entity-level analysis
- Analytical documentation

### Tools

- Databricks
- SQL
- Jupyter Notebooks
- GitHub

---

# 📚 What I Learned

Through this project, I strengthened my understanding of how to approach a real-world analytical dataset systematically.

### Key learning outcomes

- Breaking a complex dataset into meaningful business entities
- Exploring multiple related tables independently
- Using SQL to investigate data characteristics
- Identifying potential data-quality issues
- Understanding relationships between marketplace entities
- Translating data structures into business questions
- Organizing analytical work into reusable notebooks
- Documenting an analytics project professionally

---

# 📌 Project Status

**Current Stage:** 🔎 Exploratory Data Analysis

**Completed:**

- ✅ User Table EDA
- ✅ Properties EDA
- ✅ Hosts EDA
- ✅ Booking EDA
- ✅ Reviews EDA
- ✅ Amenities EDA

The project is structured to progress from **data exploration** toward deeper business and marketplace analytics.

---

# 👩‍💻 Author

## Shweta Vanarse

**BCA Graduate | Data Analyst Fresher**

Passionate about transforming raw data into meaningful business insights using:

**SQL • Python • Excel • Power BI • Tableau • Databricks**

### Connect with me

🔗 **GitHub:**  
https://github.com/shwetavanarse

🔗 **LinkedIn:**  
https://linkedin.com/in/shweta-vanarse-aa82313b1

---

## ⭐ Project

If you find this project useful or interesting, consider giving the repository a ⭐.

> **Exploring data. Finding patterns. Creating insights.** 📊
