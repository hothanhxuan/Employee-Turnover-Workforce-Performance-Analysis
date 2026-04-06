# 🧑‍🤝‍🧑 Project 3: HR Analytics Dashboard

**❓Business Question:**  
How can HR leaders understand turnover drivers (Why do employees leave?), workforce composition (How are employees distributed by department, tenure, age, and gender?), and performance trends (How are performance and engagement changing?) to improve employee retention and optimize operational decisions?

**Domain:**  
Human Resources Analytics (HR Operations)

![Image](https://github.com/user-attachments/assets/c454dbf0-a20d-4d33-bb69-bfcc26627fc8)

Author: Susan Ho  
Date: 2025-12-01  
Tools Used: Excel / Power BI  

---

## 📑 Table of Contents  
1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [⚒️ Main Process](#️-main-process)  
5. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
6. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---

## 📌 Background & Overview  

### Objective  
### 📖 What is this project about?

This project develops an **operational HR analytics dashboard** using Excel and Power BI to uncover workforce patterns, turnover behavior, and employee performance insights that drive business decisions.

✔️ Analyze employee turnover rates across departments  
✔️ Understand workforce demographics (gender, age, tenure)  
✔️ Evaluate satisfaction & engagement levels  
✔️ Identify top recruitment sources and departure reasons  
✔️ Support HR leaders with actionable insights for retention  

### 👤 Who is this project for?

✔️ HR Analysts & HR Managers  
✔️ People Operations & Talent Acquisition Teams  
✔️ Business Leaders & Department Heads  
✔️ Workforce Planning & Organizational Development Teams  

---

## 📂 Dataset Description & Data Structure  

### 📌 Data Source  
- **HRDataset.xlsx**  
  - Format: Excel (.xlsx)  
  - Rows: 311 (employees)  
  - Columns: 20+ HR attributes (demographics, performance, termination, satisfaction)

### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used  
Only one main HR dataset was used:  
- **Employee Master Table (Fact table)** — includes demographics, job info, performance, satisfaction, termination, recruitment source, etc.
- Contains details employees information (**311 records**).

| Column Name | Description |
|-------------|-------------|
| EmployeeID | Unique employee identifier |
| ManagerID | Manager supervising the employee |
| PositionID | Role/position code |
| MaritalStatusID | Marital status classification |
| PerformanceScore | Performance rating |
| Location | Work location |
| Birthday | Date of birth |
| Gender | Gender identity |
| CitizenDesc | Citizenship |
| RaceDesc | Racial group |
| Date of Hire | Hire date |
| RecruitmentSource | Hiring source |
| EmploymentStatus | Active / Terminated |
| Salary | Current salary |
| SatisfactionScore | Level of satisfaction |
| EngagementScore | Engagement rating |
| AbsenceDays | Total days absent |


#### 2️⃣ Data Relationships  

![Image](https://github.com/user-attachments/assets/38047a1c-6e57-45f5-a630-3d4dada177a9)

| **From Table** | **To Table** | **Join Key**   | **Relationship Type**                                  |
|------------|----------|------------|----------------------------------------------------|
| `Employee`   | `Position`| `PositionID` | Many-to-One (multiple employees belong to one position) |
| `Employee`   | `MaritalStatus`| `MaritalStatus ID` |  Many-to-One (multiple employees belong to one marital status) |
| `Employee`   | `Performance`| `PerfScoreID` | Many-to-One (multiple employees belong to one performance score) |
| `Department`   | `Position` | `DeptID`   | Many-to-One (multiple positions belong to one department) |

---

## 🧠 Design Thinking Process  

**1️⃣ Empathize**  
HR leaders need fast, accurate insights about workforce structure, turnover reasons, and engagement.

**2️⃣ Define Point of View**  
“How might we help HR understand the root causes of turnover and maintain an optimized workforce?”

**3️⃣ Ideate**  
Dashboard ideas included:  
- Turnover analysis  
- Satisfaction & engagement insights  
- Demographic breakdown  
- Recruitment efficiency  
- Department performance benchmarking  

**4️⃣ Prototype and Review**  
Created Power BI dashboard iterations and refined based on stakeholder feedback.

---

## ⚒️ Main Process  

### 1️⃣ Data Cleaning & Preprocessing  
✔ Removed empty header rows  
✔ Standardized date formats  
✔ Derived Age and Tenure fields  
✔ Normalized employment status names  
✔ Removed duplicate employee records  

### 2️⃣ Exploratory Data Analysis (EDA)  
Explored:  
- Salary by department  
- Distribution of tenure and age  
- Termination reasons  
- Satisfaction score patterns  
- Recruitment source effectiveness  

### 3️⃣ Power BI Measures (DAX)  
Examples of measures created:  
- **Turnover Rate**  
- **Absence Rate**  
- **Average Tenure**  
- **Average Satisfaction Score**  
- **Average Engagement Score**

### 4️⃣ Power BI Visualization  
Developed a 2-page dashboard covering:  
- Workforce Overview  
- Turnover & Department Metrics  
- Recruitment vs Termination Insights  
- Employee Detail View  

---

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Executive Summary

![Image](https://github.com/user-attachments/assets/fb194ecd-ddf7-4984-b872-dfbf1dc4ad6b)

**Main Findings:**  
- Total employees: **299**  
- Turnover rate: **34.78%**  
- Avg tenure: **12.31 years**  
- Absence rate: **0.23%**  
- Avg satisfaction score: **3.89/5**  
- Avg engagement score: **4.11/5**

**Interpretation:**  
The company has a mature workforce but faces turnover challenges that may affect stability and productivity.

---

### 1️⃣ Turnover Drivers – Why do employees leave?

| Reason | Number of employees | % of total turnover |
|--------|------------------|------------------|
| Another position | 20 | 18.7% |
| Unhappy | 14 | 13.1% |
| Higher salary | 11 | 10.3% |
| Personal/Other | 36 | 33.6% |
| Unknown | 20 | 18.7% |

**Analysis:**  
- Production department has the **highest turnover: 40.69%**  
- Main reasons: career growth, salary, job satisfaction  
- IT/Software Engineering has **high engagement >4.0** → lower turnover  

---

### 2️⃣ Workforce Composition – Who are our employees?

| Metric | Value | Notes |
|--------|-------|------|
| Total employees | 299 |  |
| Gender | 52% Male, 48% Female |  |
| Average age | 36.5 |  |
| Average tenure | 12.31 years |  |
| Turnover by department | Production 40.69%, Sales 16.13%, IT/Software 33.33% | Focus on high-turnover departments |

**Analysis:**  
- Workforce is experienced (avg tenure 12.31 years)  
- Turnover is concentrated in Production and mid-tenure employees (5–15 years)  
**Interpretation:**  
Production may require targeted retention programs, while Sales' practices could serve as a model for other departments.
---

### 3️⃣ Performance Trends – How is performance and engagement?

| Metric | Company average | Notable departments |
|--------|----------------|------------------|
| Performance score | 3.85 / 5 | IT/Software >4.0 |
| Engagement score | 4.11 / 5 | IT/Software >4.0 |
| Relationship with turnover | Low engagement → high turnover | Production, mid-tenure |

**Analysis:**  
- Higher engagement → better performance → lower turnover  
- Low satisfaction or engagement → higher risk of leaving  
- HR should focus on programs to improve engagement and performance 

---

### 4️⃣ Recruitment & Termination Insights  

**Top Recruitment Sources:**  
- Indeed: 82 hires  
- LinkedIn: 74 hires  

**Top Termination Reasons:**  
| Reason | Number of employees | % of total turnover |
|--------|------------------|------------------|
| Another position | 20 | 18.7% |
| Unhappy | 14 | 13.1% |
| Higher salary | 11 | 10.3% |

**Analysis & Interpretation:**  
- Recruitment is concentrated on **Indeed and LinkedIn**, which covers most hires. HR may consider diversifying sources for future recruitment.  
- **Turnover reasons** show that most separations are avoidable: career growth (another position), dissatisfaction (unhappy), and salary (higher pay elsewhere).  
- Departments with high turnover (e.g., Production 40.69%) match these reasons, indicating HR should focus on **retention strategies** in these areas.  
- Improving **compensation, career development, and workplace satisfaction** could directly reduce turnover and improve performance.  

### 🔍 Dashboard Workforce Database 
![Image](https://github.com/user-attachments/assets/ca274757-2134-429a-ad61-db5cd032376b)
---

## 🔎 Final Conclusion & Recommendations  

### 📌 Key Takeaways  
✔ High turnover rate suggests a need for stronger retention strategies  
✔ Production department faces significant churn issues  
✔ Satisfaction & engagement levels vary across departments  
✔ Recruitment relies heavily on Indeed & LinkedIn  
✔ Exit reasons indicate internal improvement opportunities  

### 📌 Recommended Actions  
✔ Implement retention initiatives focused on Production  
✔ Review compensation competitiveness  
✔ Provide more career mobility opportunities  
✔ Enhance onboarding & engagement frameworks  
✔ Diversify recruitment sources  

---
