# AIS HCA Healthcare Challenge

## Project Overview
This project analyzes HCA hospital locations and disaster risk data to assess hospital preparedness, staffing levels, and resource availability in high-risk areas. Our goal is to improve disaster response planning through data-driven insights.

### Participants
- **Alesandro Rodriguez**  
- **Christopher Sequeira**  

## Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Importance](#why-its-important)
- [Approach](#approach)
- [Analytical Approach](#analytical-approach)
- [High-Level Workflow](#high-level-workflow)
- [Dataset](#dataset)
- [Data Preprocessing](#preprocessing--cleaning-steps)
- [Results & Insights](#results--insights)
- [Project Structure](#project-structure)

---

## Overview
Our mission is to enhance patient assistance through optimized resource allocation, emergency preparedness, and disaster relief, ensuring timely and efficient care. Natural disasters disrupt hospital operations due to inadequate resource distribution and uneven workforce allocation. This project aims to mitigate these challenges by improving emergency response strategies.

### Problem Statement
Hospitals in disaster-prone areas require better preparedness and resource allocation to maintain effective patient care during emergencies. However, staffing shortages and inefficient resource distribution often lead to operational inefficiencies during disasters.

### Why It’s Important
- Disasters increase patient demand and disrupt hospital functions, making efficient staff allocation critical.
- Some hospitals in high-risk areas may lack adequate resources, while others may have surplus capacity.
- Understanding disaster frequency and severity at a county and state level helps optimize preparedness efforts.

---

## Approach
- Merged HCA hospital data with FEMA disaster data to assess hospital risk at the state and county levels.
- Assigned risk categories based on historical disaster frequency.
- Analyzed hospital staffing levels in high-risk vs. low-risk areas.
- Mapped high-risk counties to potential nearby counties that could serve as backup facilities.

### Analytical Approach
- **Exploratory Data Analysis (EDA):** Identified patterns in disaster frequency, risk categories, and hospital staffing using **Tableau**.
- **Risk Classification:** Categorized disaster-prone states into risk levels (Low, Medium, High) using disaster count thresholds.

### High-Level Workflow
#### 1. Data Collection & Cleaning
- Combined **HCA hospital dataset** with **FEMA disaster data**.
- Standardized state and county fields for proper merging.

#### 2. Risk Analysis
- Categorized states into **risk levels based on disaster frequency**.
- Compared **staffing levels vs. disaster risk**.

#### 3. Visualization & Insights
- **U.S. Map** highlighting high-risk states and counties.
- **Scatter plot** comparing hospital staffing levels vs. disaster risk.

---

## Dataset
- **Source:** HCA Data was provided by HCA. FEMA data sourced from [FEMA Data Resources](https://hazards.fema.gov/nri/data-resources).

### Dataset Summary
- **Number of Rows:** 238,221
- **Number of Columns:** 21

### Key Variables
#### HCA Hospital Data
- `HCA_facility_city`, `HCA_facility_state`, `HCA_county_updated`: Hospital location details.
- `HCA_EmpDepartment`, `HCA_EmpPositionDesc`: Employee role and department information.
- `HCA_Tenure`: Employee tenure in years.

#### Disaster Risk Data
- `Risk_Categories`: Disaster risk classification (e.g., High Risk, Medium Risk).
- `disaster_count`: Total recorded disasters per county/state.

#### Disaster Types
- Coastal Storm, Earthquake, Fire, Flood, Hurricane, Tornado, Winter Storm, etc.

---

## Preprocessing & Cleaning Steps
### 1. Standardized Location Data
- Merged **HCA hospital data** with **FEMA disaster dataset** using **state and county**.
- Cleaned inconsistencies in **county names** for accurate joins.

### 2. Assigned Disaster Risk Categories
- Created `Risk_Categories` based on **disaster_count thresholds**.

### 3. Dealing with Missing Data
- Filled missing **county-level information** where possible.

---

## Results & Insights
We developed a **data-driven approach** to identify high-risk counties, assess workforce vulnerability, and guide resource allocation for **HCA’s disaster planning**. Our analysis highlights counties facing the highest disaster impact and workforce strain, enabling decision-makers to optimize emergency response.

### Key Findings
- A **three-zone relief strategy** optimizes emergency preparedness:
  - **Primary Zone:** Immediate evacuations.
  - **Secondary Zone:** Reinforcing medical support.
  - **Tertiary Zone:** Long-term recovery efforts.
- **Population size** plays a role in resource allocation, with larger counties requiring more medical personnel.
- **Real-time monitoring systems & dashboards** are essential for tracking disaster trends, employee distribution, and resource availability.
- Integrating **external data sources and operational planning** will further strengthen disaster preparedness efforts.

---

## Project Structure
```
/code           # Code & Tableau files
/data           # Project datasets
/figures        # PNG images & plots
/presentations  # Presentation slides
.gitignore      # Hidden Git instructions
.python-version # Python version control
requirements.txt # Dependencies for reproducible environment
```

---
