# National-Rail-Ticket-Sales-Analysis
This repository contains a Power BI project analyzing National Rail's ticket sales data from December 2023 to April 2024 sourced from [Maven Analytics](https://mavenanalytics.io/challenges) The dashboard provides insights into popular routes, peak travel times, revenue by ticket type and class, and on-time performance, helping National Rail make data-driven decisions. 

## Project Background
The National Rail Ticket Sales Analysis project was developed to provide valuable insights into the ticket sales and operational performance of National Rail, a major provider of passenger train services in England, Scotland, and Wales. The dataset sourced from Maven Analytics, covering the period from December 2023 to April 2024, includes key information such as transaction details, ticket types, journey times, and reasons for delays.

## Business Objectives
- Identify Popular Routes: Determine which routes are most frequently traveled to optimize scheduling and resource allocation.
- Determine Peak Travel Times: Analyze travel data to identify peak times, aiding in capacity management and service planning.
- Analyze Revenue Distribution: Examine revenue from different ticket types and classes to understand financial performance and potential areas for growth.
- Diagnose On-Time Performance: Investigate punctuality and identify factors contributing to delays and cancellations to improve service reliability.

## Overview of the Data
The dataset provided for this project contains mock train ticket sales data for National Rail in the UK, covering the period from December 2023 to April 2024. The data cleaning and transformation process was conducted in Excel before uploading to Power BI for analysis. Here is a detailed overview of the key transformations and final columns included in the dataset:

**Major Transformations in Excel:**
- Removal of Duplicates: Ensured unique records by removing duplicate entries in the Transaction ID column.
- Removal of Unwanted Columns: The dataset initially contained multiple columns, some of which were removed to streamline the analysis. Unnecessary columns were identified and excluded to focus on relevant data.
- Removal of Blank Rows: Blank rows were eliminated to maintain the integrity and completeness of the data.
- Formatting Text Columns: Applied text transformations such as Clean, Trim, and Capitalize to columns like Departure Station, Arrival Destination, and Railcard for consistency and readability.
- Calculating New Columns: Created new columns such as Route by concatenating Departure Station and Arrival Destination, and Journey Duration by calculating the time difference between Departure Time and Arrival Time.
  
**Final Columns in the Maven Railway Table:**
- Transaction ID: Unique identifier for each ticket transaction.
- Date of Purchase: The date on which the ticket was bought.
- Time of Purchase: The exact time the ticket purchase was made.
- Purchase Type: Indicates whether the purchase was online, at a ticket counter, etc.
- Purchase Method: The payment method used, such as credit card or cash.
- Railcard: Information on whether a railcard was used and the type of railcard.
- Ticket Type: The type of ticket, such as single, return, or season ticket.
- Ticket Class: The class of the ticket (e.g., Standard or First Class).
- Price: The cost of the ticket.
- Departure Station: The station from which the journey begins.
- Arrival Destination: The station where the journey ends.
- Date of Journey: The date the journey takes place.
- Departure Time: The scheduled time the train departs.
- Arrival Time: The scheduled time the train arrives.
- Actual Arrival Time: The actual time the train arrived at the destination.
- Journey Status: The status of the journey, indicating whether it was on-time, delayed, or cancelled.
- Reason for Delay: If applicable, the reason for any delay encountered.
- Refund Request: Indicates whether a refund was requested for the journey.
- Route: Created by concatenating the Departure Station and Arrival Destination to represent the travel route.
- Journey Duration: The duration of the journey, calculated as the difference between Departure Time and Arrival Time.

## Tools and Technology Used

1. **Microsoft Excel:**
- Data Cleaning: Removed duplicates, unwanted columns, and blank rows.
- Data Transformation: Calculated journey duration, concatenated departure and arrival stations to form routes.
- Data Preparation: Ensured data consistency and accuracy before importing into Power BI.
  
2. **Power BI:**
- Data Modeling: Imported cleaned data from Excel, created relationships between tables, and built calculated columns and measures.
- Data Visualization: Designed interactive dashboards with various visualizations such as bar charts, column charts, line charts, and pie charts.
- Slicers and Filters: Added slicers for ticket class, ticket type, and date of journey to enable dynamic filtering of the data.
- Insight Generation: Developed insights on popular routes, peak travel times, revenue analysis, and on-time performance.
  
3. **Power Query Editor:**
- Data Transformation: Applied additional data transformations and cleaning steps within Power BI to refine the dataset.
- Advanced Filtering: Implemented complex filtering and data shaping techniques to prepare the data for visualization.

## Project Workflow
A Project Workflow provides a good structure for every data analytics project. It helps to establish a clear roadmap of sequential steps from the initial problem to the final insights. This keeps the project organized and aligned with goals. It also outlines tasks within each project phase, preventing important elements from being overlooked and making the process more efficient. The workflow for this project is shown below:

![project workflow](https://github.com/Debbiefolorunsho/National-Rail-Ticket-Sales-Analysis/blob/main/Project%20Workflow.png?raw=true)

## 1.  Project Objective
The main objective of this project is to analyze National Rail's ticket sales data from December 2023 to April 2024 to provide meaningful insights into the most popular routes, peak travel times, revenue analysis by ticket types and classes, and on-time performance. This analysis aims to help National Rail improve operational efficiency and enhance passenger experience.

## 2.  Data Collection
The dataset used for this project includes mock train ticket sales data for National Rail in the UK, covering the period from January to April 2024. The data encompasses various attributes related to each ticket purchase and journey, including Transaction ID, date and time of purchase, purchase type and method, railcard information, ticket type and class, price, departure and arrival stations, journey dates and times, actual arrival time, journey status, reason for delay, and refund requests.

## 3.  Data Cleaning and Preparation
The initial data cleaning and preparation were carried out using Microsoft Excel:

- Removal of Duplicates: Ensured uniqueness in the Transaction ID column.
- Removal of Unwanted Columns: Eliminated unnecessary columns to streamline the analysis.
- Removal of Blank Rows: Removed rows with missing values to ensure data completeness.
- Journey Duration Calculation: Calculated journey duration using the departure and arrival times.
- Route Creation: Concatenated departure and arrival stations to form a 'Route' column.
After the initial cleaning in Excel, the data was uploaded to Power BI for further transformation and analysis. Additional data shaping and cleaning steps were performed using the Power Query Editor in Power BI.
Data Model
After the initial cleaning in Excel, the data was uploaded to Power BI for further transformation, modeling, and analysis. In Power BI:

**Data Model Creation:** A new date table was created and linked to the main railway table to enable time-based analysis.
Measures: The following measures were created for detailed analysis:
- Total Revenue: Calculated by summing up the price column.
- Average Ticket Price: Calculated as the average of the price column.
- Delay Duration: Calculated by the difference between actual arrival time and scheduled arrival time.
- Route Count: Counted the occurrences of each unique route

## Data Analysis & Visualization
After completing the data cleaning and preparation, I proceeded with the analysis and visualization phase. 

**Key Insights from the Data Visualization**

![national rail dashboard 1](https://github.com/Debbiefolorunsho/National-Rail-Ticket-Sales-Analysis/blob/main/National%20rail%201.jpg?raw=true)

**Overview:**

The overview section indicates that a total revenue of £742,000 was generated from 32,000 journeys. The majority of journeys (87%) were on time, while 7% were delayed, and 6% were canceled. The data highlights the primary routes experiencing delays and cancellations, as well as the ticket classes and purchase types contributing to the overall revenue.

**Total Revenue Analysis**
- By Year and Month: January 2024 had the highest revenue at £200K, followed by a dip in February to £159K, with a recovery in March (£195K) and April (£188K). This fluctuation suggests possible seasonal variations or operational changes affecting monthly revenues.
- By Purchase Type: Online purchases accounted for £383K, while station purchases contributed £359K. This trend highlights the increasing preference for digital ticketing.
  
**Journey Status Analysis**
- On Time: 87%
- Delayed: 7%
- Cancelled: 6%
  
Most journeys are on time, but efforts can be made to reduce the percentage of delayed and canceled journeys.

![national rail dashboard 2](https://github.com/Debbiefolorunsho/National-Rail-Ticket-Sales-Analysis/blob/main/National%20rail%202.jpg?raw=true)

**Delay Analysis**

**Top 5 Routes Encountering Delays:**
- Liverpool Lime Street to London Euston: 19.8 delays
- Manchester Piccadilly to Liverpool Lime Street: 16.5 delays
- London Euston to Birmingham New Street: 9.2 delays
- Manchester Piccadilly to Leeds: 6.4 delays
- Manchester Piccadilly to London Euston: 4.0 delays
  
**Delay Duration by Reasons:**
- Weather: 24.6
- Signal Failure: 16.2
- Staff Shortage: 9.5
- Technical Issue: 8.2
- Weather Condition: 3.6
- Staffing: 3.1
- Traffic: 2.0
  
The data points out the major routes and reasons for delays, suggesting areas for operational improvements.

**Revenue by Ticket Class**
- Standard Class: £593K
- First Class: £149K
- Standard Class generates the most revenue, indicating higher demand for more affordable travel options.
  
## Recommendations
Based on the analysis and key insights derived from this project, the following recommendations can help drive improvements and increase revenue for National Rail in 2024:

**1. Optimize Online Sales Promotions:**
- Continue to promote online ticket purchases, as they contribute significantly to the revenue. Offering discounts or incentives for online purchases can further boost sales.

**2. Address Operational Inefficiencies:**
- Focus on the routes with the highest delays and cancellations. Implementing measures to address weather impacts and signal failures could improve on-time performance.
  
**3. Enhance Customer Experience:**
- Improve services during peak travel times to manage the high volume of passengers effectively. This could include better resource allocation and scheduling adjustments.
  
**4. Promote Advance Ticket Sales:**
- Since advance tickets generate the highest revenue, creating promotional campaigns encouraging early bookings can lead to more stable revenue streams.
  
**5. Regional Marketing Efforts:**
- Target regions with high growth potential for marketing efforts. For example, the success in online ticket sales suggests a digital marketing focus might yield good results.
  
**6. Reduce Delay Causes:**
- Prioritize resolving issues related to weather, signal failures, and staff shortages, as these are the leading causes of delays. Proactive measures can enhance reliability.
  
**7. Adapt to Travel Trends:**
- Monitor travel trends and adjust services accordingly. For instance, increasing capacity on popular routes or times can meet demand more efficiently.
  
## Conclusion
The analysis provides a comprehensive understanding of the current performance and operational challenges faced by National Rail. By implementing the recommendations, National Rail can optimize its operations, enhance customer satisfaction, and increase revenue in 2024.
