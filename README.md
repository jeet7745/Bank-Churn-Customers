
# Bank Customer Churn Analysis

## Project Overview

Designed an interactive Power BI dashboard to analyze customer churn trends in a banking dataset. The report includes key performance indicators (KPIs) and advanced DAX measures to provide actionable insights for customer retention and engagement.

### Key Contributions:

- Developed a data model in Power BI using Power Query for data transformation and relationships.

- Designed interactive dashboards featuring KPI Cards, Bar Charts, Heatmaps, and Gauge Charts.

- Implemented DAX calculations to measure churn rate, retention rate, and customer segmentation.

- Applied filtering techniques for dynamic analysis by demographics, financial data, and product holdings.

- Key Performance Indicators (KPIs) & DAX Measures

### 1. Customer Churn Rate

#### Formula (DAX):

- Churn Rate = DIVIDE(COUNTROWS(FILTER(CustomerData, CustomerData[Churn] = 1)), COUNTROWS(CustomerData))

- Purpose: Measures the percentage of customers who left the bank.

- Visualization: KPI Card, Gauge Chart.

### 2. Customer Retention Rate

#### Formula (DAX):

- Retention Rate = 1 - [Churn Rate]

- Purpose: Measures the percentage of customers retained.

- Visualization: KPI Card, Trend Line Chart.

### 3. Churn by Demographics

#### Breakdown by:

- Country (France, Spain, Germany)

- Gender (Male, Female)

- Age Groups (18-25, 26-40, 41-60, 60+)

- DAX Example:

Churn By Country = CALCULATE([Churn Rate], ALLEXCEPT(CustomerData, CustomerData[Country]))

- Purpose: Identifies customer segments with high churn risk.

- Visualization: Bar Charts, Heatmaps.

### 4. Financial & Credit Metrics

- Credit Score Impact on Churn: Compares average credit scores of churned vs. retained customers.

- Balance & Salary Influence: Do customers with higher balances churn less?

- DAX Example:

Avg Balance Churned = CALCULATE(AVERAGE(CustomerData[Balance]), CustomerData[Churn] = 1)

- Visualization: Box Plots, Comparative Bar Charts.

### 5. Product & Engagement Metrics

- Product Holding Influence: Measures churn rate based on the number of products held.

- Active Membership Impact: Compares churn rates for active vs. inactive members.

- Credit Card Ownership: Evaluates the impact of having a credit card on churn.

- DAX Example:

Churn Active Members = CALCULATE([Churn Rate], CustomerData[ActiveMember] = 1)

- Visualization: Stacked Bar Charts, Pie Charts.

### Report Structure in Power BI

- Overview Page: Displays high-level KPIs (Churn Rate, Retention Rate, Total Customers).

- Demographics Page: Churn breakdown by country, gender, and age.

- Financial Impact Page: Relationship between churn, balance, salary, and credit score.

- Engagement Page: Analysis of product holdings, credit cards, and active membership.

### Business Impact & Insights

- Developed insights to identify high-risk customer segments and churn drivers.

- Recommended targeted retention strategies based on age, country, and product usage.

- Suggested financial incentives for customers with low engagement.

- Enabled personalized marketing strategies based on credit score and product interactions.

### Technical Skills Applied:

- Power BI (Data Modeling, Report Building, Advanced Visualizations)

- DAX (Calculated Measures, Filtering, Aggregations)

- Power Query (Data Transformation, Cleaning, and Relationship Management

