# HR Analytics Dashboard (Power BI)

An interactive, end-to-end Power BI dashboard designed to transform raw workforce data into actionable HR insights. This project focuses on analyzing employee demographics, department distributions, and driving forces behind employee attrition to support data-driven talent retention strategies.

---

## 🎯 Project Overview & Objective
Organizations face significant costs and disruptions when high-performing talent exits unexpectedly. The core objective of this project is to provide HR leadership with a centralized tool to:
1. **Track Key Workforce Metrics:** Monitor real-time KPIs like active headcount, average age, and tenure.
2. **Identify Attrition Drivers:** Pinpoint correlations between employee departures and variables like salary brackets, job satisfaction, department, and experience level.
3. **Facilitate Strategic Planning:** Empower stakeholders to filter data dynamically to isolate risk factors and design targeted retention interventions.

---

## 🛠️ Tech Stack & Tools Used
*   **Data Visualization & Analytics Platform:** Power BI Desktop
*   **Data Transformation Engine:** Power Query
*   **Analytical Expressions:** DAX (Data Analysis Expressions)
*   **Dataset:** Structured HR Dataset (~1,480 employee records across 37 columns)

---

## ⚡ Key Features & Deliverables

### 1. Robust Data Preprocessing (Power Query)
*   **Data Hygiene:** Isolated and removed duplicate employee logs and cleared rows containing critical null values to establish a clean analytical baseline.
*   **Inconsistency Resolution:** Structured textual variables (e.g., standardized uneven formatting in categories like `Business Travel`) using structural find-and-replace queries.
*   **Schema Optimization:** Re-evaluated and locked automated data type assignments (such as converting age parameters from strings to integers) to safeguard against downstream measure failures.

### 2. Advanced DAX Architecture & KPI Framework
*   Formulated complex calculated fields and distinct measures, including an exception-safe attrition rate utilizing the `DIVIDE` function to systematically avoid division-by-zero errors.
*   Structured a modular KPI ribbon tracking:
    *   **Total Employees** | **Active Employees** | **Attrition Count**
    *   **Attrition Rate (%)** | **Average Age** | **Average Experience (Years)**

### 3. Multi-Dimensional Visualizations
*   **Demographic & Structural Footprints:** Implemented Doughnut, Funnel, and Pie charts to illustrate department-wise allocations, gender distribution, and age groups (e.g., segmenting specific generations).
*   **Compensation Analysis:** Deployed Clustered Bar charts charting the intersection of salary slabs (LPA) against turnover volumes.
*   **Risk Matrix:** Configured a conditionally formatted Matrix cross-referencing granular job roles against discrete job satisfaction ratings to highlight pockets of low engagement.
*   **Tenure Trends:** Built an Area Chart tracking attrition spikes across different career stages and organizational life cycles.

### 4. User-Centric Interactivity
*   Integrated tile-styled dynamic slicers across core dimensions (`Department` and `Age Group`), allowing users to completely filter the entire visual interface in a single click.

---

## 📂 Project Structure
```text
├── hr_analytics_dataset.csv     # The raw source data file
├── HR_Analytics_Dashboard.pbip  # Completed Power BI workbook file
├── Screenshots/
│   └── dashboard_preview.png       # UI/UX preview images
└── README.md                        # Project documentation
