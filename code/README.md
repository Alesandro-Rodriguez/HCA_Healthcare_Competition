# Code

## FEMA Dataset Cleaning
Here, we have our file to reformat the FEMA dataset. 

## Prep File
We also have our prep file, where we joined our two datasets together to create our final dataset.

- In clean step 1, we added a calculated field to add missing data
- We also renamed fields to have HCA in front of them. This makes it so we could identify which column belonged to which dataset in our final dataset
- In clean step 4, we split up 'designatedArea' to separate the word 'county' from our counties
- From there we did a left join keepiong all of the HCA_hospitals data on state and county.
- In clean step 3, we changed some of the data types to geographic data types (HCA_facility_state, HCA_facility_city, and HCA_county_updated).


## Tableau File
We also have our Tableau file to show how we made our visualizations.
