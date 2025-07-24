## 📊 Healthcare Waitlist Analysis – Power BI Dashboard

### 🔍 Project Overview  
This Power BI report analyzes **patient waiting lists** in the healthcare sector (2018–2021). 
It provides insights into current patient volumes, historical trends, and specialty/age-level breakdowns for **Inpatient** and **Outpatient** cases. 
Built for healthcare decision-makers, the report supports data-driven operational planning.

---

![Healthcare Report - Power BI](https://github.com/user-attachments/assets/8e90c426-7c8d-4848-a629-1eb76990fe52)


### 🎯 Business Problems Addressed  
Healthcare administrators needed a solution to:  
1. **Track** current status of waitlists  
2. **Analyze** historical trends across case types  
3. **Drill down** by age and medical specialty  

---

## 1: Requirement Gathering  
- Mapped key stakeholders (ops leads, analysts)  
- Defined goals via stakeholder conversations  
- Finalized KPIs: *Average Waitlist*, *Median Waitlist*, *Total Current Waitlist*  
- Outlined scope and timelines for development  

---

## 2: Data Collection  
- Used **Folder Connector** in Power BI  
- Loaded Inpatient and Outpatient CSVs for scalable data management  

---

## 3: Data Transformation (Power Query)  
- Standardized column names  
- Added missing fields (`Case_Type`, `Age_Profile`)  
- Appended data into a single unified table: `All_Data`  
- Trimmed and replaced values for cleanliness  

---

## 4: Data Modeling  

- Built clean relationships and hid unnecessary tables  
- Optimized model size and performance  

---

## 5: Dashboard Design & DAX Measures  
- Designed custom background layout (using PNG)  
- Created **toggle slicers** for Average/Median view  
- Added **dynamic titles**, **no-data messages**, and **tooltips**  
- Built DAX measures for latest month, prior year, and case filters  

```DAX
Dynamic Title = 
SWITCH(
   VALUES('Calculation Method'[Calc Method]),
   "Average", "Key Indicators - Patient Wait List (Average)",
   "Median", "Key Indicators - Patient Wait List (Median)"
)
```

#### Report Pages

- Summary Page
  
1. KPI Cards (Current Waitlist, PY Comparison)
2. Case Type Doughnut Chart
3. Monthly Trend Line Chart
4. Top Specialties by Volume
5. Filters: Date, Specialty, Case Type

- Detailed View
  
1. Matrix by Archive Date, Specialty, Age Profile, Time Band
2. Supports drill-through and deep filtering

![Detailed View](https://github.com/user-attachments/assets/fc7db10e-f407-4247-a072-8bdfeef7ea16)



## Outcome | Impact for Stakeholders

This report enables:

- Instant visibility into current waitlist loads
- Historical performance monitoring
- Prioritization by specialty and age
- A single, unified source of insights for hospital planning teams
- It replaces time-consuming manual reviews with fast, filterable, and actionable insights.

 📁 **Project files are attached for reference**  

  #### I'm always open to feedback, collaborations, or discussing data projects. Feel free to reach out via GitHub or LinkedIn!
