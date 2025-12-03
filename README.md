# HR Attrition & Workforce Insights Dashboard – Power BI

## 📸 Dashboard Preview

### Main Dashboard
<img width="1226" height="686" alt="image" src="https://github.com/user-attachments/assets/3e1ea242-2125-438d-974d-708775021e34" />

### Key Influencers View & Tenure vs Attrition
<img width="442" height="676" alt="image" src="https://github.com/user-attachments/assets/6617ca99-aedb-46e6-ae16-64b8997182bf" />

<img width="441" height="677" alt="image" src="https://github.com/user-attachments/assets/e8d6971d-c6e2-4496-bb84-cb8411a2a195" />


## 📌 Project Overview

This project is an interactive **HR Analytics dashboard** built in **Power BI** to help HR teams
understand **employee attrition** and key workforce trends.  
It combines a core HR dataset, engagement survey data, and geographic information to answer questions like:

- What is our employee attrition pattern?
- Which groups are most at risk of leaving?
- How is our workforce distributed by age, gender, tenure, and location?

---

## 🎯 Objectives

1. Check overall **attrition rate** of employees.  
2. Analyse **staff gender distribution**.  
3. Understand **age distribution** of employees.  
4. View an **overview of people’s work locations** on a map.  
5. Measure the **impact of tenure (YearsAtCompany)** on attrition.  
6. Use **Key Influencers** to identify other drivers of attrition (e.g. overtime, job level, marital status).

---

## 🧩 Data & Modelling

- Imported **two main datasets** from Excel:
  - **Core HR dataset** – demographics, tenure, income, performance, attrition.
  - **Engagement survey dataset** – job satisfaction and survey scores.
- Performed data transformations in **Power Query**:
  - Converted `SalaryHike` to proper **percentage** by dividing by 100.
  - Converted `DailyRate` and `MonthlyIncome` to **fixed decimal currency ($)**.
  - Ensured correct **data types** for date, numeric and categorical fields.
- Added a third **GEO dataset** containing **city, latitude and longitude** to fix map issues  
  (e.g. London being mapped to the UK instead of Canada).
- Built relationships in the **Model view**:
  - `EmployeeNumber` used as a key between **Core HR** and **Engagement Survey**.
  - `Office` ↔ `City` relationship between **Core HR** and **GEO** data.

---

## 📊 Visuals & Features

Main dashboard elements:

- **KPI Cards**
  - Total Employees (1470)
  - Average Job Satisfaction
  - Average Performance Rating

- **Gender Distribution Donut Chart**
  - Shows male vs female split across the organisation.

- **Histogram: Count of Employees by Age (bins)**
  - Age grouped into bands from 18 to 60 to see age spread.

- **Map: Count of Employees by Location**
  - Bubble map using latitude/longitude from the GEO dataset.
  - Bubble size represents employee count per city in the US and Canada.

- **Histogram: Count of Employees by Years at Company with Attrition**
  - Shows attrition vs non-attrition for different tenure bands.

- **Key Influencers Visual**
  - Explores factors that increase the likelihood of **Attrition = Yes**.

---

## 🔍 Key Insights & Findings

- **Higher attrition in the first 1–2 years** of employment.  
  - The histogram shows a spike in attrition for employees with low tenure.
  - This suggests the company should focus retention efforts during the early years.

- **Overtime is a strong driver of attrition.**
  - Key Influencers show that when **OverTime = Yes**, the likelihood of attrition increases
    by roughly **2–3x** compared to the average rate.

- **Low job level employees are more likely to leave.**
  - Segments where **JobLevel ≤ 1** and **OverTime = Yes** show the highest attrition.

- **Single employees have higher attrition than married employees.**
  - Marital status appears as another important influencer.

- **Workforce is concentrated in a few major cities in the US and Canada.**
  - The map visual highlights key hubs with high employee counts, useful for location-based HR planning.

Overall, the dashboard helps HR quickly identify **at-risk groups** (new joiners, low job level, working overtime, single employees) and design targeted **retention strategies**.

---

## 🛠️ Tools & Skills

- **Power BI Desktop**
  - Power Query for data cleaning and transformation
  - Data modelling with relationships
  - DAX measures for KPIs
  - Key Influencers visual
- **Excel** (source data)
- **Geospatial mapping** using latitude/longitude
- HR Analytics & storytelling with data

---

## ▶️ How to Use

1. Download the `.pbix` file from this repository.
2. Open it in **Power BI Desktop**.
3. Refresh the data if needed (ensure the Excel files are in the same relative paths).

