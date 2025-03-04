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

# Project Summary  

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

### 4. Final Recommendations  
- Highlighted **understaffed high-risk hospitals**.  
- Suggested **potential support hospitals** for emergency assistance.   

## Dataset
- Source: HCA Data was provided by HCA themselves. We incorporated the FEMA data: [https://hazards.fema.gov/nri/data-resources] 
- Description: Briefly describe the dataset, including the number of rows/columns and key variables.
- Any preprocessing or cleaning steps performed.

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

