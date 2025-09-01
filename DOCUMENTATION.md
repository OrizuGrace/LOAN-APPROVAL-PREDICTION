# LOAN-APPROVAL-PREDICTION
## Loan Approval Prediction Dashboard

## Executive Summary
Our team developed an interactive Power BI dashboard that analyzes loan approval patterns and predicts outcomes using a comprehensive 5,000-record banking dataset. The solution addresses critical challenges in financial decision-making by providing management with actionable insights into approval trends, customer risk profiles, and predictive analytics to optimize lending strategies.
 
Image: Dashboard Landing Page Screenshot

### Project Objective
The primary goal was to create a data-driven solution that enhances loan approval decision-making through pattern recognition and predictive modeling. Our dashboard serves two purposes: analyzing historical approval trends to identify systemic issues and providing forward-looking predictions to guide future lending decisions.


### Data Preparation and Exploration
The dataset comprised 5,000 customer records with comprehensive information including demographics, account details, transaction history, loan specifications, credit card metrics, customer feedback, and anomaly detection flags.
Our data preparation process involved systematic cleaning and standardization. We consolidated customer names, standardized date formats across all tables, removed personally identifiable information like contact details, and handled duplicate records. Age categorization was implemented to enable demographic segmentation.
Statistical exploration revealed key patterns: the overall approval rate of 34.2% suggested conservative lending practices, while correlation analysis identified strong relationships between customer tenure, credit utilization, and approval outcomes. A

### Data Modeling and Feature Engineering 
Image: Data Model

We implemented a robust star schema architecture, splitting the dataset into fact and dimension tables including Loans, Customers, Transactions, Cards, and Feedback dimensions. This structure optimized query performance and enabled flexible analysis across multiple business perspectives.
Feature engineering focused on creating meaningful risk indicators. We developed a Customer Tenure metric measuring account longevity, Credit Utilization ratios for spending behavior analysis, and a binary flag identifying loans exceeding account balances. We used a composite Risk Level calculation, combining anomaly presence, credit utilization patterns, tenure, and loan-to-balance ratios into a three-level system to classify customers as low, medium, or high risk.

### Analytical Approach and Prediction Model
We developed a transparent rule-based prediction system aligned with business logic. Our model categorizes applications into "Likely Approved," "Likely Rejected," and "Needs Review" based on the engineered Risk Level and supporting factors.
The prediction logic prioritizes interpretability while maintaining reasonable accuracy. Low-risk customers with established tenure and healthy credit utilization patterns receive "Likely Approved" predictions, while high-risk profiles with anomalies or excessive loan-to-balance ratios are flagged for rejection. The "Needs Review" category captures edge cases requiring human judgment.

### Dashboard Architecture and Visualization
The dashboard comprises five interconnected pages designed for different analytical perspectives:
* Loan Overview Page serves as the executive dashboard, displaying critical KPIs including 5,000 total loans with a 34.2% approval rate and $25.5K average loan amount. The monthly trend analysis reveals seasonal patterns in application volume, while loan distribution charts break down performance by type (Mortgage, Auto, Personal) and term length. The visualization effectively balances high-level metrics with detailed breakdowns.
 
* Image: Loan Overview Dashboard Screenshot
* Customer Insight Page provides comprehensive demographic analysis through an interactive geographic map showing loan distribution across 40 cities, complemented by gender and tenure segmentation charts. The age and utilization rate analysis reveals that older customers show higher approval rates, while the 63.2% average utilization rate indicates healthy credit management across the customer base.
 
* Image: Customer Insight Dashboard Screenshot

* Risk & Anomaly Page focuses on risk assessment, highlighting that 300 total anomalies resulted in only 108 approvals (36% approval rate for anomalous cases). The risk level distribution shows balanced representation across low, medium, and high-risk categories, with the anomaly impact clearly visualized through comparative approval rates.
 
Image: Risk & Anomaly Dashboard Screenshot
Prediction Analysis Page validates our model performance with detailed accuracy metrics showing 50.9% prediction accuracy. The page includes a comprehensive customer-level prediction table demonstrating individual case analysis, while the forecast chart projects loan applications through 2025, supporting strategic capacity planning.
 
Image: Prediction Analysis Dashboard Screenshot
Landing Page consolidates key insights and navigation, ensuring seamless user experience across all analytical dimensions.
Key Insights and Findings
Our analysis uncovered several critical patterns with significant business implications. While the overall loan approval rate stands at 34.2%, this number hides deeper differences across customer groups. For example, applications flagged as anomalies were much less likely to be approved as only about 36% got through, compared to much higher rates for clean applications.
The prediction model achieved 50.9% accuracy when excluding "Needs Review" cases, revealing gaps between systematic risk assessment and actual decision-making. Many low-risk applications faced rejection while some high-risk cases received approval, indicating either unmeasured factors influencing decisions or inconsistent application of lending criteria.
Geographic analysis revealed significant risk concentration in specific branches, suggesting either market-specific factors or operational inconsistencies requiring management attention.
Recommendations
The dashboard provides immediate value through enhanced visibility into lending operations. Management can now identify underperforming segments, monitor approval trends in real-time, and allocate resources based on predicted application volumes.
Based on the insights, we recommend the following:
˗	Developing more nuanced rules for the “Needs Review” segment, possibly by identifying new risk indicators not yet considered
˗	Exploring machine learning in the future, while keeping the explainability of the current rule-based approach to support non-technical users
˗	Standardizing decision-making across branches to reduce inconsistencies and ensure fair, risk-aware approvals
˗	Reviewing mismatches where high-risk customers were approved or low-risk ones rejected, to improve decision quality and build trust in the system.


Conclusion
This dashboard transforms raw lending data into strategic insights, providing management with the tools needed to optimize approval processes, manage risk effectively, and plan for future growth. The combination of historical analysis and predictive capabilities creates a comprehensive solution addressing both operational efficiency and strategic planning needs.
The 50.9% prediction accuracy, while modest, establishes a baseline for continuous improvement and highlights specific areas where enhanced data collection or refined logic could drive better outcomes. Most importantly, the dashboard's design ensures findings translate directly into actionable business decisions, maximizing the value of data-driven lending strategies.
