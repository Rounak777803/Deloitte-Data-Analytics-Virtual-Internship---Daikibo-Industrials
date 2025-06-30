# 📊 Deloitte Data Analytics Virtual Internship - Daikibo Industrials
This repository showcases the work completed during the Deloitte Data Analytics Virtual Internship program on The Forage platform. This simulation provided hands-on experience in solving real-world business problems by leveraging data analysis, transformation, and visualization techniques using Power BI.

**✨ Project Overview**
The internship focused on two key business challenges for Daikibo Industrials: analyzing machine telemetry data to identify breakdown patterns and investigating internal complaints regarding gender pay inequality. The project involved a full data analytics lifecycle, from data ingestion and transformation to generating actionable insights.

**🛠️ Technologies & Tools Used**
Microsoft Power BI Desktop: Primary tool for data loading, transformation (Power Query Editor), data modeling, DAX calculations, and interactive dashboard creation.

**Power Query (M-Code):**
For advanced data cleaning, reshaping, and custom transformations (e.g., Unix timestamp conversion).

**DAX (Data Analysis Expressions):**
For creating calculated columns and measures to derive key performance indicators and apply business logic.

**JSON:**
Source format for telemetry data.

**Excel/CSV:**
Source format for equality data.

# 📈 Key Analytical Tasks & Deliverables
## Task 1: Machine Telemetry Data Analysis (Daikibo Factories)
**Objective:** 
To identify the factory with the most machine breakdowns and the specific machines that broke most often within that location, quantifying potential downtime.

**Data Source:**
daikibo-telemetry-data.json (containing one month of May 2021 telemetry data from 4 factories, 9 machine types, messages every 10 mins).

Key Steps & Deliverables:

Data Ingestion & JSON Flattening:

Loaded the nested JSON telemetry data into Power BI.

Performed extensive data transformation in Power Query Editor to flatten the hierarchical JSON structure into a clean, tabular format, expanding nested Record and List types (e.g., location and data objects).

Timestamp Conversion:

Implemented a custom M-code formula in Power Query to accurately convert Unix timestamps (milliseconds since Epoch) from the timestamp column into a proper Date/Time format, resolving data type errors.

Data Cleaning & Renaming:

Renamed columns (e.g., location.country to Country, data.status to Status) for enhanced readability and usability.

Ensured correct data types (Decimal Number for Temperature).

Breakdown Quantification (DAX Measure):

Created a calculated DAX measure named "Unhealthy" that assigns a value of 10 for every non-"healthy" status reading (Status <> "healthy"), effectively quantifying 10 minutes of potential downtime per unhealthy status.

Insight Generation & Visualization:

Developed a "Down Time per Factory" bar chart (or similar visual) to identify the factory with the highest total Unhealthy minutes (most significant breakdown location).

Created a subsequent visual to pinpoint the Device Types that contributed most to downtime within the identified top breakdown factory.

## Task 2: Gender Pay Equality Analysis (Daikibo Industrials)
**Objective:**
To classify and analyze gender pay equality scores across various job roles and factory locations based on an externally provided "Equality Score."

**Data Source:**
Task 5 Equality Table.xlsx (containing Factory, Job Role, and Equality Score).

Key Steps & Deliverables:

Data Ingestion:

Loaded the Equality Table.xlsx dataset into Power BI.

Equality Classification (DAX Calculated Column):

Created a new DAX calculated column named "Equality Class" to categorize the Equality Score based on predefined business rules:

Fair: Score between -10 and +10 (inclusive).

Highly Discriminative: Score less than -20 OR greater than +20.

Unfair: All other scores (between -20 and -10, or between +10 and +20, exclusive of highly discriminative).

Analysis Readiness:

The newly created Equality Class column provides a clear categorical variable for further analysis and visualization of gender pay equality across the organization.

**💡 Key Learnings & Skills Demonstrated**
Data Ingestion & ETL: Proficiently handling diverse data sources (JSON, CSV) and complex data structures.

Advanced Power Query (M-Code): Expertise in data transformation, cleaning, and custom formula creation for complex data types (e.g., Unix timestamps).

DAX (Data Analysis Expressions): Skilled in creating robust calculated measures and columns for business logic and KPIs.

Data Analysis & Classification: Ability to extract meaningful insights and categorize data based on business rules.

Business Intelligence & Data Visualization: Competent in building foundational visualizations to answer specific business questions.

Problem-Solving: Addressed real-world data challenges (e.g., messy JSON, business rule implementation) to deliver actionable results.

Certificate:https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/9PBTqmSxAf6zZTseP/io9DzWKe3PTsiS6GG_9PBTqmSxAf6zZTseP_wg2z4fkWmpP3j4RSn_1744391901597_completion_certificate.pdf
