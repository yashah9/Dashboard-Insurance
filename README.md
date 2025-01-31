# Insurance Claim Analysis Dashboard

## Project Overview
This project involves the creation of a dashboard for analyzing insurance claims. The dashboard visualizes key metrics such as claim amounts, premium amounts, policy activity, and demographics, providing actionable insights.

## Data Sources
InsData.csv

## Tools and Technologies
- **MS SQL Server**: Used for database management and querying.
- **Excel**: Utilized for initial data storage and sharing.
- **Power BI**: Built the dashboard for visualizing data and generating insights.
- **Power Query**: Enabled transformations, column creation, and data cleaning.

## Data Cleaning and Preparation
- Added new columns for determining active/inactive policies based on current date and policy end date.
- Adjusted data types using locale settings to ensure consistency across fields.
- Created user roles (e.g., Travel Policy Manager) to restrict data visibility based on roles.
- Scheduled automatic data refreshes in Power BI to maintain up-to-date visuals.
- Validated refresh functionality by adding new data to the database and observing changes in visuals.

## Exploratory Data Analysis (EDA)
Explored the dataset to identify trends, patterns, and outliers:
- Counted claims by policy type, claim status, and customer demographics.
- Analyzed premium and claim amounts across age groups and policy categories.

## Data Analysis
### Code for Active/Inactive Policy Calculation in Power Query
```powerquery
ActiveStatus = if [EndDate] >= DateTime.LocalNow() then "Active" else "Inactive"
```
![dash](https://github.com/user-attachments/assets/44b2fd55-3f3b-4245-bbd0-19f66837d01e)

---
### Drill-Through Functionality
The dashboard includes drill-through features to provide a deeper dive into KPIs:
- Drill-through allows users to focus on individual claims, policies, or customer details by right-clicking on a data point and navigating to detailed views.
- Enabled easy navigation between summary-level insights and granular data for actionable analysis.

![Travel](https://github.com/user-attachments/assets/aacccac6-f6c5-49f7-ad84-1d6b90bcf661)

## Results and Findings
- **Policy Insights:** Travel insurance generated the highest premiums, while home insurance had the lowest.
- **Claim Trends:** The majority of claims were rejected, with pending claims being the least.
- **Demographic Analysis:** Adults accounted for the highest claim amounts, while young adults had the least.
- **Activity Metrics:** 78% of policies were active, highlighting customer engagement.
  
## Limitations
- The analysis is limited to the data available in the current database and may not account for external factors.

- Scheduled refreshes are dependent on consistent data entry and database updates.

## References
[Microsoft Power BI](https://learn.microsoft.com/en-us/power-bi/)

[MS SQL Server](https://learn.microsoft.com/en-us/sql/sql-server/?view=sql-server-ver16)

[Power Query](https://learn.microsoft.com/en-us/power-query/)
