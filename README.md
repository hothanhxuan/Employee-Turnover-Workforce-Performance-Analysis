# 📊 HR Analytics Dashboard  

**Business Question:**  
How can HR leaders understand turnover drivers, workforce composition, and performance trends to improve employee retention and optimize operational decisions?

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

### 1️⃣ Workforce Overview  

**Main Findings:**  
- Total employees: **299**  
- Turnover rate: **34.78%**  
- Avg tenure: **12.31 years**  
- Absence rate: **0.23%**  
- Avg satisfaction score: **3.89**  
- Avg engagement score: **4.11**

**Interpretation:**  
The company has a mature workforce but faces turnover challenges that may affect stability and productivity.

---

### 2️⃣ Department Analysis  

**Key Metrics:**  
- Production turnover: **40.69%** (highest)  
- Sales turnover: **16.13%** (lowest)  
- IT/IS & Software Engineering show high engagement (>4.0)

**Interpretation:**  
Production may require targeted retention programs, while Sales' practices could serve as a model for other departments.

---

### 3️⃣ Recruitment & Termination Insights  

**Top Recruitment Sources:**  
- Indeed (82 hires)  
- LinkedIn (74 hires)  

**Top Termination Reasons:**  
- Another position (20)  
- Unhappy (14)  
- More money (11)  

**Interpretation:**  
Most separations are avoidable with improvements in compensation, career growth, and workplace satisfaction.

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
