# Logistics-Performance-Analysis: Documentation: Logistics Analysis Using Excel Power Pivot


Project Title: Comprehensive Logistics Performance Dashboard Using Excel Power Pivot

Objective

To build a scalable and interactive logistics analytics model in Excel using Power Pivot. The goal is to track freight movement, analyze vehicle and driver performance, optimize fuel and maintenance costs, and understand customer distribution.


### Dataset Sources: The dataset is sourced from Kaggle.


Data Model Overview: 

The model includes:

Table Name	          Description

Customer	            contains location and demographic data per customer

Drivers	              Master list of drivers and metadata

Vehicles	            Trucks and trailer information

Dim_Date	            Standard date dimension to support time intelligence

Fact_KMTraveled	      Fact table tracking distance travelled, fuel usage, cost and efficiency

Fact_Freight	        Freight transaction table including revenue, weight, and goods value

All relationships are one-to-many, anchored by dimension tables (Date, Driver, Vehicle, Customer) to their corresponding fact tables.


Data Cleaning and Preparation

Loaded data using Power Query with consistent data types.

Standardised column names and ensured referential integrity across tables.

Null or blank values were handled via default fallbacks or filtering.

Created calculated columns for derived metrics such as Total KM, Fuel Cost, and Maintenance per Truck.

Key DAX Measures: A robust set of KPIs were created using DAX, including but not limited to:


Operational Metrics

Total KM Travelled

Fuel Efficiency = KM Traveled / Liters

Maintenance per Truck

Average Cost per KM = Total Cost / KM Travelled



Financial Metrics

Gross Profit = Net Revenue - Total Cost

Total Revenue

Revenue per KM = Total Revenue / KM Travelled

Revenue per KG = Revenue / Weight


Aggregated Insights

Trips per Truck

Revenue per Driver

YoY Growth (from Dim_Date)

YTD Revenue

These measures are used across PivotTables, Slicers, and visual summaries.


Dimensions for Analysis

Dimension	Key Attributes	Used For

Date	Year, Month, Week, Quarter	Time-based analysis

Driver	Name, ID	Performance benchmarking

Vehicle	Truck Type, Brand, Year	Fleet performance

Customer	City, State, Geo-coordinates	Geographic distribution


Dashboard Insights

The resulting dashboard offers interactive analysis across several logistics angles:


Driver & Vehicle Performance

Top drivers by KM and revenue

Vehicles with the highest fuel efficiency and maintenance cost


Freight Analysis

Revenue by truck type and route

Cost per KM and profit margins by load weight

Average goods value across regions


Customer Mapping

Heat map of customers by state/city

Density by latitude and longitude


Time Intelligence

YTD vs Previous Year revenue

Monthly and quarterly performance

Week-on-week delivery trends


Key Takeaways

Trailer trucks contributed more significantly to profit, while some brands underperformed in fuel efficiency.

Certain drivers achieved outstanding cost/km metrics, making them optimal for long hauls.

Customer locations in high-density areas corresponded with higher freight volume but thinner margins due to cost pressure.

Maintenance and fuel are primary cost drivers—monitoring them with KPIs helps optimise fleet usage.



🛠️Tools and Features Used

Power Pivot: For data modelling and relationships

DAX: For dynamic KPIs and calculations

Power Query: Data transformation

PivotTables & PivotCharts: Interactive visual analysis

Slicers & Timelines: Dashboard interactivity


Conclusion

This project showcases the power of Excel Power Pivot in turning raw logistics data into a scalable, insightful dashboard. 

It supports strategic decisions around fleet management, driver assignment, and delivery planning, making it a valuable asset for logistics and operations managers.

