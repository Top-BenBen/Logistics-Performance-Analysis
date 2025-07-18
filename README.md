# Logistics Performance Analysis Documentation

**Project Title**: Comprehensive Logistics Performance Dashboard Using Excel Power Pivot

Objective

To build a scalable and interactive logistics analytics model in Excel using Power Pivot. The goal is to track freight movement, analyze vehicle and driver performance, optimize fuel and maintenance costs, and understand customer distribution.


### Dataset Sources: The dataset is sourced from Kaggle.

### Data Model Overview: The model includes the table name & their description.

**Customer**: Contains location and demographic data per customer

**Drivers**: Master list of drivers and metadata

**Vehicles**: Trucks and trailer information

**Dim_Date**: Standard date dimension to support time intelligence

**Fact_KMTraveled**: Fact table tracking distance travelled, fuel usage, cost and efficiency

**Fact_Freight**: Freight transaction table including revenue, weight, and goods value

##### All relationships are one-to-many, anchored by dimension tables (Date, Driver, Vehicle, Customer) to their corresponding fact tables.

<img width="1366" height="768" alt="Screenshot (192)" src="https://github.com/user-attachments/assets/cf4373d5-9ca9-4a54-81f8-4b4915fbbc55" />



### Data Cleaning and Preparation

**Loaded data using Power Query with consistent data types.**

**Standardised column names and ensured referential integrity across tables.**

**Null or blank values were handled via default fallbacks or filtering.**

**Created calculated columns for derived metrics such as Total KM, Fuel Cost, and Maintenance per Truck.**


### Key DAX Measures: A robust set of KPIs were created using DAX, including but not limited to:
##### Operational Metrics :
Total KM Travelled, 
Fuel Efficiency = KM Travelled / Liters,
Maintenance per Truck and
Average Cost per KM = Total Cost / KM Travelled


##### Financial Metrics:
Gross Profit = Net Revenue - Total Cost, 
Total Revenue,
Revenue per KM = Total Revenue / KM Travelled, and 
Revenue per KG = Revenue / Weight.


##### Aggregated Insights:
Trips per Truck, 
Revenue per Driver, 
YoY Growth (from Dim_Date) and
YTD Revenue.

**These measures are used across PivotTables, Slicers, and visual summaries.**


##### Dimensions for Analysis:                               
Date (Year, Month, Week, and Quarter) was used for Time-based analysis

Driver	Name and  ID were used for Performance benchmarking

Truck Type, Brand, and Year	were used for Fleet performance

Customer	City, State and Geo-coordinates were used for Geographic distribution


### Dashboard Insights: The resulting dashboard offers interactive analysis across several logistics angles:

##### Driver & Vehicle Performance: Top drivers by KM and revenue, Vehicles with the highest fuel efficiency and maintenance cost

##### Freight Analysis: Revenue by truck type and route, Cost per KM and profit margins by load weight and Average goods value across regions.

##### Customer Mapping: Heat map of customers by state/city and Density by latitude and longitude.

##### Time Intelligence: YTD vs Previous Year revenue,  Monthly and quarterly performance and Week-on-week delivery trends. 

<img width="1366" height="768" alt="Screenshot (189)" src="https://github.com/user-attachments/assets/547fe28b-12e3-4604-bb6c-68b511f1433e" />


### Key Takeaways
Trailer trucks contributed more significantly to profit, while some brands underperformed in fuel efficiency.

Certain drivers achieved outstanding cost-per-kilometre metrics, making them optimal for long-haul routes.

Customer locations in high-density areas corresponded with higher freight volume but thinner margins due to cost pressure.

Maintenance and fuel are primary cost drivers—monitoring them with KPIs helps optimise fleet usage.


### Tools and Features Used

**Power Pivot**: For data modelling and relationships

**DAX**: For dynamic KPIs and calculations

**Power Query**: Data transformation

**PivotTables & PivotCharts**: Interactive visual analysis

**Slicers & Timelines**: Dashboard interactivity


### Conclusion

This project demonstrates the power of Excel Power Pivot in transforming raw logistics data into a scalable and insightful dashboard. 

It supports strategic decisions around fleet management, driver assignment, and delivery planning, making it a valuable asset for logistics and operations managers.

Click [`here`](https://www.loom.com/share/62c3604a4682441ab128bd69d7a9f450?sid=f647a49d-1e51-405a-b49d-acf29c62acce) for details in the video.
