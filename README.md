# Earrings-from-Buses---PowerBi

Summary Report — Earnings from Buses Analysis 
1. Dataset Overview 
The dataset contains bus-earning information across multiple Indian cities from 2015–2018, 
including: 
• Average No. of daily trips 
• Average No. of passengers per day 
• Average trip length (km) 
• Average cost per km (₹) 
• Revenue per km (₹) 
• City & Year 
A total of 125 records exist, covering 4 years and 30+ cities. 
2. Data Cleaning Performed 
✔ Removed invalid rows 
• Records with missing passenger count, trip length, or revenue were cleaned. 
• Converted incorrectly formatted numeric columns (e.g., strings with “.00”, commas). 
✔ Standardized formats 
• Year values standardized to integer. 
• All financial values converted to numeric type. 
✔ Created proper Date/Year structures 
Unique year dimension created (YearUnique) for stable relationships. 
✔ Checked and removed duplicates 
• Ensured unique City-Year combinations. 
3. Data Transformations Performed 
A. Calculated Columns (Earnings from Buses) 
Column 
Purpose 
Cost Per Day 
Trips × TripLength × Cost/km 
Trips × TripLength × Revenue/km 
Revenue Per Day 
Duration (Years) 
EndYear – StartYear 
Total Distance 
Trips × TripLength 
Year Range 
StartYear – EndYear 
Passenger Growth  
Flags growth: Increase/Decrease 
B. DAX Measures Created 
Measure 
Meaning 
Total Passengers 
SUM of passengers 
Total Revenue 
SUM of Revenue/day 
Total Trips 
SUM of trips 
Total Cost 
SUM of Cost/day 
Total Distance 
SUM of Distance 
Total Profit 
Revenue – Cost 
YoY Passengers % 
Growth % 
YoY Passengers Change 
Difference YoY 
4. Data Modeling 
A Star Schema model was created: 
✔ Fact Table 
Earnings from Buses 
✔ Dimensions 
• Location (City & City ID) 
• YearUnique (distinct Year) 
✔ Relationships 
Location[City ID] → Earnings[City ID] 
DimYearUnique[Year] → Earnings[Start Year] 
This ensures clean filtering across visuals. 
5. Visuals Used in Dashboard 
Dashboard 1 — City Performance 
1. KPI Cards: 
Total Passengers, Total Revenue, Total Trips, Total Cost, Avg Trip Length, Total 
Distance, Total Profit. 
2. Column + Line Chart: 
Year-wise Total Passengers & Revenue. 
3. Horizontal Bar: 
City-wise Total Passengers. 
4. Doughnut Chart: 
Share of Revenue by City. 
5. Map Visual: 
Passenger Trend Classification by City. 
6. Clustered Bar: 
Total Trips & Total Distance (City × Year). 
7. Column Chart: 
Passenger Volume vs Growth Flag. 
Dashboard 2 — Revenue & Insights 
1. Gauge / Donut: Total Revenue. 
2. Area Chart: Revenue by Year × Passenger Growth Flag. 
3. Waterfall Chart: Total Distance by Growth Class. 
4. Bar Chart: Profitability Status (Profitable vs Not). 
5. Smart Narrative: Automatically generated insights. 
6. Insights (Summary) 
✔ City Revenue Distribution 
• Raipur contributed the highest revenue (~65% share). 
• Belagavi & Bareilly contribute moderate revenue. 
✔ Passenger Trends 
• Passenger count peaked in 2017, then sharply dropped by 2018. 
✔ Profitability 
• Profitable cities travelled significantly higher distances. 
• Passenger Growth Flag strongly correlates with profitability. 
✔ Revenue vs Cost 
• Some cities have high cost per km but low revenue, indicating inefficiencies. 
7. Final Output 
A complete Power BI solution consisting of two optimized dashboards: 
 
Dashboard 1 → City Performance 
(Operational metrics: trips, passengers, distance, trends) 
 
Dashboard 2 → Revenue & Insights 
(Financial metrics: revenue, cost, profit, profitability groups) 
Executive Summary  
• The analysis reveals strong passenger volumes concentrated in major cities, with 
Raipur leading in both revenue and trip counts. 
• Year-wise trends show steady passenger movement from 2015–2017, followed by a 
decline in 2018. 
• Profitability varies by city, with several locations showing high revenue despite lower 
trip counts. 
• Cost-per-km vs revenue-per-km analysis highlights significant efficiency differences 
across cities. 
• Overall, the dashboard provides clear insights into passenger flow, revenue 
distribution, and operational performance for strategic decision-making. 
