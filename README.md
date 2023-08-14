# Solar-analysis
Project Documentation: Solar Energy and Battery Model
# Purpose of the Model
The purpose of this model is to analyze and optimize the utilization of solar energy and a battery storage system to reduce electricity costs for Naomi. The model takes into account solar panel electricity generation, electricity usage, battery charge, electricity price variations, and inflation rates to calculate projected savings and assess the feasibility of investing in a battery system.
# Data and Checks
Data Source
The data used in this project was gotten from the 'Junior Data Analyst _ Data.xlsx' file.
Data Cleaning
•	Outliers were detected using the Interquartile Range (IQR) method and removed to ensure data quality.
•	Data was aggregated at both hourly and monthly levels for analysis.
# Assumptions
1.	Solar panel  electricity generation, electricity usage, and battery performance data provided in the dataset are accurate and representative of real-world conditions.
2.	The battery's capacity remains constant at 12.5 kWh.
3.	Electricity prices follow the provided inflation rates.
# Methodology
1.	Data Cleaning and Exploration: The raw data was loaded into a Pandas DataFrame. Outliers were identified and removed using the IQR method. Descriptive statistics were calculated to understand the data's distribution and characteristics.
2.	Data Aggregation and Analysis: Hourly and monthly aggregations of solar generation, electricity usage, and battery performance were calculated. These aggregations were used to analyze trends and patterns in energy usage and generation.
3.	Battery Charge: Battery charge levels were calculated based on the excess solar electricity generated and the electricity needed. The battery's performance was bounded by its capacity (12.5 kWh). Electricity bought from the battery and savings were derived from these calculations.
4.	Cost and Savings Analysis: The cost of electricity purchased with and without the battery was calculated for each hour and aggregated monthly. The difference in costs represented the potential savings from using the battery.
5.	Scenario Analysis: Two scenarios were analyzed:
•	Scenario 1: Government-expected electricity price increase of 4% p.a.
•	Scenario 2: Naomi's estimated electricity price increase starting at 4% p.a. and rising by an additional 0.25% p.a., with a discount rate of 6% p.a. Net Present Value (NPV) was calculated for both scenarios to assess their financial viability.
6.	Internal Rate of Return (IRR): The IRR was calculated using the fsolve function to find the discount rate that equates the NPV to the initial cost of the battery for each scenario.
# Conclusion
The developed model provides insights into the potential benefits of implementing a battery storage system alongside solar panel. By analyzing scenarios of electricity price increases and inflation rates, the model evaluates the financial feasibility and returns on investment associated with such an endeavor. 

