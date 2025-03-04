# AIS HCA Healthcare Challenge
The project analyzes HCA hospital locations and disaster risk data to assess hospital preparedness, staffing levels, and resource availability in high-risk areas for better disaster response planning.

# Participants
Alesandro Rodriguez
&
Christopher Sequeira

## Table of Contents
- [Overview](#Overview)
- [Dataset](#dataset)
- [Results & Insights](#results--insights)
- [Project Structure](#project-structure)

## Overview
Our mission is to enhance patient assistance through optimized resource allocation, emergency preparedness, and disaster relief, ensuring timely, equitable, and efficient care.

During natural disasters, patient care is affected due to inadequate resource allocation and uneven workforce distribution across HCA facilities. The plan aims to improve emergency response and resource management.

## Project Summary  

## Problem Statement  
Hospitals in disaster-prone areas need better preparedness and resource allocation to ensure effective patient care during emergencies. However, staffing shortages and poor resource distribution in high-risk areas can lead to operational inefficiencies during disasters.  

## Why It’s Important  
- Disasters disrupt hospital operations and increase patient demand, requiring efficient staff allocation.  
- Some hospitals in high-risk areas may lack adequate resources, while others nearby might have surplus capacity.  
- Understanding disaster frequency and severity at a county and state level helps optimize preparedness efforts.  

## Approach  
- Merged HCA hospital data with FEMA disaster data to assess hospital risk at the state and county level.  
- Assigned risk categories to hospitals based on historical disaster frequency.  
- Analyzed hospital staffing levels in high-risk vs. low-risk areas to identify potential staffing shortages.  
- Mapped hospitals to potential nearby locations that could serve as backup facilities.  

## Analytical Approach  
- **Exploratory Data Analysis (EDA)** to identify patterns in disaster frequency, risk categories, and hospital staffing (In Tableau).  
- **Risk classification** using disaster count thresholds (e.g., Low, Moderate, High, Severe).  

## High-Level Workflow  
### 1. Data Collection & Cleaning  
- Combined **HCA hospital dataset** with **FEMA disaster data**.  
- Standardized state and county fields for proper merging.  

### 2. Risk Analysis  
- Categorized hospitals into **risk levels based on disaster frequency**.  
- Compared **staffing levels vs. disaster risk**.  

### 3. Visualization & Insights  
- **U.S. Map** highlighting high-risk states and counties.  
- **Scatter plot** comparing hospital staffing levels vs. disaster risk.   

## Dataset
- Source: HCA Data was provided by HCA themselves. We incorporated the FEMA data: [https://hazards.fema.gov/nri/data-resources] 

## Dataset Description  

## Number of Rows  
- 238,221  

## Number of Columns  
- 21  

## Key Variables  

### **HCA Hospital Data**  
- `HCA_facility_city`, `HCA_facility_state`, `HCA_county_updated`: Location details of the hospital.  
- `HCA_Emp34Id`: Unique employee ID.  
- `HCA_EmpDepartment`, `HCA_EmpDepartmentName`, `HCA_EmpPositionDesc`: Employee role and department information.  
- `HCA_MgrTitle`: Manager title.  
- `HCA_EmpAnnivDate`, `HCA_EmpPositionIsSuper`, `HCA_EmpRNExperienceDate`: Employment details such as tenure and position level.  
- `HCA_Tenure`: Employee tenure in years.  

### **Disaster Risk Data**  
- `Risk_Categories`: Disaster risk classification (e.g., High Risk, Medium Risk).  
- `state`, `designatedArea - Split 1`: State and county details from disaster dataset.  
- `disaster_count`: Total number of recorded disasters in the county/state.  

### **Disaster Types**  
- `Coastal Storm`, `Dam/Levee Break`, `Earthquake`, `Fire`, `Flood`, `Hurricane`, `Mud/Landslide`, `Other`, `Severe Ice Storm`, `Severe Storm`, `Snowstorm`, `Straight-Line Winds`, `Tornado`, `Tropical Storm`, `Volcanic Eruption`, `Winter Storm`.  

---

## Preprocessing & Cleaning Steps  

### **1. Standardized Location Data**  
- Merged **HCA hospital data** with **FEMA disaster dataset** using **state and county**.  
- Cleaned inconsistencies in **county names** (`HCA_county_updated`) for accurate joins.  

### **2. Assigned Disaster Risk Categories**  
- Created `Risk_Categories` field based on **disaster_count** using thresholds:  
  - **Low Risk:** 0-50  
  - **Moderate Risk:** 51-150  
  - **High Risk:** 151-300  
  - **Severe Risk:** 301+  

### **3. Dealing with Missing Data**  
- Ensured **all states are represented** in the dataset, even if no disaster data existed.  
- Filled missing **county-level information** where possible.  

## Results & Insights
- Summarize key findings with visuals if possible (attach images or link to a report).
- What patterns, relationships, or predictions did you discover?
- How can these insights be applied in a real-world setting?

## Project Structure
- `/code` Scripts with prefixes (e.g., `01_import-data.py`,
  `02_clean-data.py`) and functions in `/code/src`.
- `/data` project data sets.
- `/figures` PNG images and plots.
- `/presentations` Presentation slides.
- `.gitignore` Hidden Git instructions file.
- `.python-version` Hidden Python version for the reproducible
  environment.
- `requirements.txt` Information on the reproducible environment.

