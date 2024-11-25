# Valuating Scheibler House 

This repository contains the R code and dataset used to predict the price of the Scheibler House, a historic property designed by a renowned architect, to be sold after renovations. The project applies data cleaning, feature engineering, and regression analysis to estimate the house's value.

# Project Overview
The goal of this project is to:
1. Prepare and clean property and sales datasets.
2. Develop predictive models to estimate housing prices.
3. Apply adjustments to account for unique architectural value and market trends.

# Key Challenges:
1. Estimating the added value of historical architectural design.
2. Limited comparable sales data.
3. Accounting for price trends and market variations.

# Dataset
The project uses two primary datasets:
1. Sale Data: Contains historical sale information for various properties. https://data.wprdc.org/dataset/real-estate-sales
2. Characteristics Data: Includes property attributes like lot area, number of bedrooms, and year built.
https://data.wprdc.org/dataset/property-assessments

# Data Preparation:
1. Cleaned datasets by removing irrelevant columns and handling missing data.
2. Created new features such as AGE_SALE, TOTALBATHS, and SALE_YEAR.
3. Filtered data to include only valid sales and properties in relevant zip codes.

# Two Approaches for Valuation
Approach 1: Linear Regression Model
- Developed a linear regression model using log-transformed sale prices to improve model fit.
- Key predictors:
1. Property characteristics: CONDITIONDESC, BEDROOMS, FINISHEDLIVINGAREA, TOTALBATHS, etc.
2. Neighborhood fixed effects and time variables like SALE_YEAR.
- Adjusted the year factor to 2023 for prediction consistency.

Approach 2: Comparables Analysis
- Identified properties with similar characteristics to the Scheibler House.
- Applied adjustment factors for:
1. Time: Accounting for price changes over the years.
2. Neighborhood: Accounting for location-specific price variations.
- Estimated the adjusted price of comparable properties using a manual adjustment factor.

# Results
- Approach 1: Linear regression predicts the log-transformed sale price of the Scheibler House, leveraging key property attributes and fixed effects.
- Approach 2: Comparable property analysis refines the valuation by considering similar properties and applying necessary adjustments.

# Key Findings:
1. Historical design adds complexity in valuation.
2. Neighborhood and year significantly influence housing prices.
3. Log-transformed sale prices improve model accuracy.


# How to Run the Code (Two ways)
1. Clone the repository:
git clone https://github.com/TiffanyJiayue/Valuating_ScheiblerHouse.git
# OR
2. Open the R Markdown file (Valuating_ScheiblerHouse.Rmd) in RStudio; run the chunks sequentially.

# Contact
For questions or suggestions, feel free to reach out via GitHub
