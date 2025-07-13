# UK Bank Customers Analysis

![Insert Dashboard Screenshot Here]()

---

## 🚀 Introduction

The **UK Bank Customers Analysis** dashboard is an interactive and insightful business intelligence solution built using **Microsoft Power BI**. It aims to provide an in-depth understanding of customer demographics, account balances, regional concentration, and banking behavior. By leveraging this data, bank stakeholders can uncover actionable trends and make informed decisions regarding marketing, customer engagement, and regional strategies.

---

## 🛠️ Power BI and Analytics Skills Demonstrated

- **Power Query Editor** for data cleaning, transformation, and calculated columns  
- **Data modeling** using a star schema  
- **Use of relationships and cardinality**  
- **Slicers and filters** for interactivity  
- **Visual storytelling** using bar, line, column, doughnut, and map charts  
- **KPI cards** for executive summary insights  

---

## 📚 Table of Contents

[Problem Statement](#problem-statement)  
[Data Sourcing](#data-sourcing)  
[Data Transformation and Cleaning](#data-transformation-and-cleaning)  
[Data Modeling](#data-modeling)  
[Analysis and Visualization](#analysis-and-visualization)  
[Conclusion and Recommendation](#conclusion-and-recommendation)  

---

## Problem Statement

Key questions explored:

- What is the total, average, and per-customer bank balance?  
- Who are the top 5 customers by total balance?  
- How are customers distributed across different age groups, genders, and job classifications?  
- How does customer distribution vary by region?  
- What is the quarterly trend in account openings?  
- What is the gender balance among bank customers and how does this relate to account balances?  
- Which job classifications have the highest cumulative account balances?  

---

## Data Sourcing

- **Source:** [Kaggle – UK Bank Customers](https://www.kaggle.com/datasets/ukveteran/uk-bank-customers)  
- **Format:** CSV  
- **Size:** 4,015 rows × 9 columns  
- **Columns:**  
  - Customer ID  
  - Name  
  - Surname  
  - Gender  
  - Age  
  - Region  
  - Job Classification  
  - Date Joined  
  - Balance  

---

## Data Transformation and Cleaning

**Tools used:** Power Query Editor in Power BI

**Steps undertaken:**

- Merged “Name” and “Surname” into a single “Customer Name” column  
- Converted “Date Joined” to proper Date format  
- Removed null values from critical fields (Customer ID, Balance, Gender)  
- Created an Age Group column (Youth, Middle Age, Prime Age) using conditional logic in Power Query  
- Trimmed whitespaces and applied consistent capitalization across text fields  
- Verified and enforced correct data types (numeric, date, text)  

![Insert Screenshot of Power Query Steps Here]()

---

## Data Modeling

A **star schema** model was developed with `Customer` ID acting as the primary key linking the dimension and fact tables:

- **Customer Dim Table:**  
  Fields: Customer ID, Customer Name, Gender, Age, Age Group, Region, Job Classification  
- **Account Details Table:**  
  Fields: Customer ID, Date Joined, Balance  

**Relationships:**  
- One-to-many relationship between Customer Dim and Account Details (via Customer ID)

![Insert Screenshot of Data Modeling View Here]

---

## Analysis and Visualization

Each visualization directly answers questions from the problem statement:

### 1. KPI Cards

- **Total Bank Balance:** `£159,622,523.37`
- **Number of Customers:** `4,014`
- **Average Bank Balance:** `£39,766.45`

![Insert Screenshot of KPIs]()

---

### Top 5 Customers by Total Balance (Bar Chart)

| Customer Name      | Total Balance      |
|--------------------|-------------------|
| Paul Reid          | £197,798.40       |
| Dorothy Jackson    | £183,467.70       |
| Carl Fraser        | £181,680.99       |
| Connor North       | £172,085.48       |
| Sebastian Arnold   | £161,517.82       |

![Insert Screenshot]()

---

### Quarterly Account Opening (Line Chart)

| Quarter | Accounts Opened |
|---------|-----------------|
| Q1      | 123             |
| Q2      | 925             |
| Q3      | 1,353           |
| Q4      | 1,613           |

![Insert Screenshot]()

---

### Customer Concentration by Region (Map Chart)

| Region           | Number of Customers |
|------------------|--------------------|
| England          | 2,159              |
| Scotland         | 1,124              |
| Wales            | 520                |
| Northern Ireland | 211                |

![Insert Screenshot]()

---

### Gender-Based Distribution (Doughnut Chart)

| Gender | Total Balance      | Percentage  |
|--------|-------------------|-------------|
| Male   | £86,638,989.30    | 54.28%      |
| Female | £72,983,534.07    | 45.72%      |

![Insert Screenshot]()

---

### Balance by Job Classification (Column Chart)

| Job Classification | Total Balance      |
|--------------------|-------------------|
| White Collar       | £78,065,883.04    |
| Blue Collar        | £41,334,055.50    |
| Other              | £40,222,584.83    |

![Insert Screenshot]()

---

### Interactive Slicers for Filtering by:

- **Age Group:** Youth, Middle Age, Prime Age  
- **Gender:** Male, Female  
- **Quarter:** Qtr 1–4  
- **Job Classification:** Blue Collar, White Collar, Other  

---

## Conclusion and Recommendation

### 🎯 **Key Insights**

- `England` hosts the majority of customers, making it a strategic location for focused growth.
- `Males` slightly outpace females in cumulative bank balance, though both represent strong segments.
- `White-collar` professionals hold the highest cumulative account balances, suggesting higher income or savings potential.
- The highest rate of account openings is in `Quarter 4`, signaling a possible seasonal trend worth exploring further.

---

### 💡 **Recommendations**

- **Targeted Marketing:** Focus campaigns in regions with high customer counts, especially England.
- **Segment Expansion:** Explore incentives or tailored services for underrepresented regions like Wales and Northern Ireland.
- **Seasonal Promotions:** Take advantage of the Q4 spike with limited-time offers or referral programs.
- **Job-Specific Products:** Introduce premium products or loyalty programs for white-collar workers to increase retention.

---

*© 2025 Douglas Boateng | [GitHub](https://github.com/dougieboat)*