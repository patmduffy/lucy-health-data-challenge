# Health vs. Wealth: A Housing-First Strategy for Malaria Mitigation in Kenya
**Authors:** Patrick Duffy, Daniel D'Alessio, and Austin Baron
*Winning Entry for the Lucy Family Institute for Data & Society’s Health Data & Analytics Challenge*

## Executive Summary
This repository contains the clinical data analysis and modeling used to determine the most effective strategies for reducing the impact of malaria within Kenya. This project supplements current research on malaria prevention, examining the best methods for reducing both the speed of initial infection and the overall disease burden.

Specifically, the models explore:
* How time-to-infection can be reduced for Eastern counties in Kenya.
* How overall malaria cases can be reduced for Western counties, which experience incidence rates over 600 times higher than Eastern counties.
* How housing structural features (e.g., wall type) act as determining predictive factors for malaria incidence nationwide.

## Core Findings
1. **Speed of Infection:** Mud walls and open eaves significantly accelerate the time-to-infection, even compared to the use of a spatial repellent, environmental conditions, or other factors. These two structural features are the primary indicators of risk, and improved model performance more significantly than a constructed housing index.
2. **Disease Volume:** Mud walls and open eaves are also the most predictive features of overall malaria cases. However, interventions like Indoor Residual Spraying (IRS) and window screens were also significantly effective at reducing the total case volume, showing greater potential for successful clinical interventions.
3. **Primary Takeaway:** Clinical interventions used in isolation are not nearly as effective as improving nationwide housing structure. As a county's average housing structural risk increases (greater proportion of mud houses vs. brick), the total burden of disease rises linearly.

## Methodology & Technical Approach
The analysis in this project leverages several statistical and machine learning methodologies:
* **Cox Time-Varying Proportional Hazards Model:** Used to assess micro-level risk and evaluate how structural variables accelerate or delay the timeline of a patient's initial malaria infection.
* **Negative Binomial Regression:** Utilized to calculate how specific factors increase or decrease a patient's cumulative annual malaria infections.
* **Linear Regression:** Applied to macro-level national data to confirm that housing structures are statistically significant predictors of malaria incidence across counties in Kenya.

## Repository Structure
The analysis can be found in `notebooks/lucy-health-data-challenge-code.ipynb`. This is structured as follows:
* **Sections 1 - 3:** Data Ingestion, Cleaning, Multi-tiered Imputation, Feature Engineering, and Exploratory Data Analysis (EDA).
* **Section 4:** Micro-Level Risk (Cox Time-Varying Proportional Hazards Model).
* **Section 5:** Overall Disease Burden (Negative Binomial Regression Model).
* **Section 6:** The Macro Context - Kenya National Analysis (Linear Regression).

## Technologies Used
* Python (`pandas`, `numpy`)
* Modeling & Statistics (`lifelines`, `statsmodels`, `scikit-learn`)
* Data Visualization (`matplotlib`, `seaborn`)

## Data Privacy
The raw data files (`.csv`) are not publicly hosted in this repository due to confidentiality agreements. The code within the notebook demonstrates the full methodology implemented using structural formats.
