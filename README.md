# PARKeasy: A Three-Phase Academic Project

This repository documents a comprehensive data analytics project developed over three academic semesters. The project, initially named "PARKeasy," evolved from a foundational database management system into a full-fledged business intelligence solution, "Boston Parking Analytics." It showcases the end-to-end lifecycle of a data product, from initial design and data management to data warehousing and interactive storytelling.

## Phase 1: Data Management for Analytics (IE 6700) ⚙️

This initial phase focused on building "PARKeasy," a system designed to solve urban parking challenges by creating a robust and efficient database.

**Objective:** To design and implement a structured database for a practical parking management application.

**Process & Technologies:** The system's architecture was first designed conceptually using EER and UML diagrams. This design was then translated into a logical relational model that was normalized to ensure data integrity. The primary implementation was done in MySQL, with a parallel implementation in a NoSQL database to handle different data structures and query types.

**Outcome:** A fully functional and normalized relational database, alongside a NoSQL counterpart, which provided the foundational data source for all subsequent analytics work.

## Phase 2: Data Warehousing & Integration (IE 6750) 🏗️

The project expanded by building a data warehouse to support advanced analytics, addressing the latency and processing limitations of a purely transactional system. This phase was tackled from both on-premise and cloud perspectives.

**Objective:** To extract data from the operational database, transform it, and load it into a structured data warehouse for complex analytical querying.

### On-Premise Approach:
- The operational database was built on PostgreSQL
- An ETL pipeline was built using Talend to extract data from the PostgreSQL OLTP database
- The data was loaded into a star schema data warehouse with fact and dimension tables. Slowly Changing Dimensions (SCD) were implemented to handle historical data updates

### Cloud Approach (AWS):
- A modern data pipeline was constructed using AWS services
- Data was ingested from Amazon RDS (PostgreSQL) and S3 into AWS Glue for serverless ETL processing
- The transformed data was stored in Amazon Redshift, a cloud data warehouse, with the workflow automated by AWS Step Functions and Lambda

**Outcome:** A robust OLAP data warehouse, available both on-premise and on the cloud, ready for business intelligence and visualization.

## Phase 3: Storytelling with Data (IE 5374) 📊

The final phase focused on transforming the warehoused data into a compelling visual narrative to drive business decisions, rebranded as "Boston Parking Analytics."

**Objective:** To create an interactive analytics dashboard and present it within a professional web interface.

### Dashboard Development:
- The OLAP schema was connected to Microsoft Power BI
- Complex measures and KPIs were created using Data Analysis Expressions (DAX)
- Four distinct dashboard pages were developed:
  - **Financial Performance Summary:** Showcasing total revenue, booking trends, completion rates, and revenue by location type
  - **Utilization & Booking Patterns:** Analyzing utilization rates for key areas, booking patterns by hour and day, and revenue breakdowns
  - **Facility Performance & Incidents:** Visualizing bookings by vehicle type, top 10 parking locations by volume, average duration by location, and a detailed incident analysis by type and severity
  - **Customer Segmentation:** Displaying member distribution across tiers, membership level conversion, and vehicle type preferences by member segment

### Web Integration:
- A polished, single-page website was built using HTML, CSS, and JavaScript
- The site introduces the project's goals, outlines key research questions, details the methodology, and seamlessly embeds the fully interactive Power BI dashboard

**Outcome:** A comprehensive data storytelling platform that makes complex parking analytics accessible, providing actionable insights for optimizing revenue, operations, and customer engagement.
