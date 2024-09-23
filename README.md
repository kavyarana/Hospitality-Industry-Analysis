Hospitality Domain – Data Analytics Project Overview (AtliQ Grands)

As part of a strategic response to declining market share and revenue, AtliQ Grands, a renowned luxury hotel chain operating across India, embarked on a transformative journey to integrate "Business and Data Intelligence." Due to rising competition and ineffective decision-making, the management sought a comprehensive solution. Their primary challenge was to understand and optimize their key business metrics using historical data to make data-driven decisions, ensuring revenue recovery and growth.

Project Background:
AtliQ Grands has operated for over two decades, with properties in four major cities: Hyderabad, Mumbai, Bangalore, and Delhi. Their room offerings span four categories: Elite, Premium, Presidential, and Standard. The company faced challenges with fragmented data from various booking platforms and sought to gain insights on performance, revenue, and customer behavior.

Project Goal:
The objective was to build a dynamic Power BI dashboard that provides key insights into revenue, occupancy, cancellations, and customer behavior. This report would enable AtliQ Grands to address its performance gaps, optimize pricing strategies, and increase bookings across different room categories.

Project Approach:
1. Data Import & Transformation:
All provided datasets were imported into Power BI:

dim_date (Date dimension)
dim_hotels (Hotel details)
dim_rooms (Room types and categories)
fact_bookings (Booking transactions)
fact_aggregated_bookings (Aggregated booking metrics)
After importing the data:

Data cleansing and transformation were performed using Power Query.
Relationships between the tables were established to create a STAR schema for optimal reporting.
2. Key DAX Calculations:
Several DAX measures and calculated columns were created to meet stakeholder requirements. Below are the critical calculations:

Revenue:
Revenue = SUM(fact_bookings[revenue_realized])

RevPAR (Revenue per Available Room):
RevPAR = DIVIDE([Revenue], [Total Capacity])

ADR (Average Daily Rate):
ADR = DIVIDE([Revenue], [Total Bookings], 0)

Occupancy %:
Occupancy % = DIVIDE([Total Successful Bookings], [Total Capacity], 0)

Cancellation %:
Cancellation % = DIVIDE([Total Cancelled Bookings], [Total Bookings])

Realisation %:
Realisation % = 1 - ([Cancellation %] + [No Show rate %])

Week-on-Week (WoW) Change (for various metrics): Custom DAX expressions were used to calculate WoW percentage change for key metrics such as Revenue, ADR, Occupancy %, and more.

3. Data Model:
The data model featured a STAR schema, optimizing reporting and analytics. This model facilitated efficient querying and calculation of key metrics across the properties, room classes, cities, and booking platforms.

4. Dashboard Creation:
The Power BI dashboard followed a mock-up provided by the stakeholders, incorporating the following key components:

Filters: City, Property, Room Class, Status, Platforms, and Time (Month/Week).
Metrics Visualizations: Key insights such as revenue, ADR, occupancy, and cancellation rates are broken down by room class, property, and city. A special focus was given to visualizing WoW changes to monitor progress.
Key Insights Gained:
Room Class Insights:
Highest Revenue: Elite Rooms generated the most revenue (553.7M).
Lowest Revenue: Standard Rooms with 305.6M.
RevPAR: Presidential Rooms led with 13.8K, while Standard Rooms trailed at 4.6K.
ADR: The Presidential Rooms had the highest average daily rate (23.4K), while Standard Rooms stood at 8K.
Property Insights:
Top Property by Revenue: AtliQ Exotica with 316M.
Lowest Revenue: AtliQ Seassons with only 65M.
RevPAR: AtliQ Exotica led with 7.8K.
City Insights:
Highest Revenue by City: Mumbai outperformed other cities, generating 660.6M in revenue.
Lowest Revenue: Delhi (290.9M).
Top RevPAR: Mumbai (8.89K).
Additional Insights:
Cancellation Rate: Provided a breakdown of the impact of cancellations across different properties and booking platforms.
Booking Platforms: The analysis highlighted which booking platforms performed best, aiding the marketing team in strategy refinement.
Final Thoughts:
This project demonstrated how a combination of historical data, advanced metrics, and intuitive dashboards could provide deep insights into operational performance. AtliQ Grands now has the tools to identify underperforming areas, optimize pricing and room availability, and enhance customer satisfaction across its properties.

Explore the Dashboard:
To interact with the dashboard and explore the insights yourself, click : https://app.powerbi.com/groups/me/reports/acfa1280-c28c-4266-b196-ea67b540fe6a/184ffdc4232afd12bf96?experience=power-bi .
