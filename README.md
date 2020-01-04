### Healthcare Analytics Homework and Project

Data source: Medicare Claims Synthetic Public Use Files (SynPUFs)<br> https://www.cms.gov/Research-Statistics-Data-and-Systems/Downloadable-Public-Use-Files/SynPUFs/index

![](medicaredata.JPG)

-- Final data transformation steps for project to predict outpatients at risk for hospital addmission due to chronic heart failure. This was the most time consuming part of our project, we found out how difficult and challenging dealing with healthcare records can be.

1. Removed the columns from the Outpatient and Inpatient datasets that weren't relevant to the project to reduce file size and renamed the columns for easier programming.
2. Determined which people in the Outpatient file were also admitted to the hospital
3. Created an HF flag for each member
4. Merged the HF flag onto the cleaned Outpatient file
5. Aggregated the Outpatient file above to achieve following:<br>
-- Limit each patient to one row of records<br>
-- Rolled up all Outpatient diagnostic codes to the highest level of ICD9 code categories<br>
6. Joined gender, race, age, BENE_ESRD_IND and all chronic disease flag data from beneficiary summary data set as predictors.

-- Dataset very unbalanced, balanced using random under-sampling.

-- Team members tried different classification algorithms.  Results for my LightGBM model shown below.

![](LightGBMSlide.JPG)
