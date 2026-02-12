# Financial-Data-Study
Power BI- Financial DashBoard

## **Objective:**
As per Client’s Request, the primary objective of this project was to design and deliver an interactive, monthly-level financial dashboard in Power BI to monitor the company’s overall financial performance for the stakeholders. The dashboard focuses on key financial KPIs, performance trends, budget vs. actuals tracking, cash flow, and working capital, , supporting timely, data-driven decision-making

### **File Name:** Financial_Dashboard_Dashboard.pbix

## Data Overview:
- The dataset comprises monthly financial and operational data, including:
  1. Profit & Loss metrics such as Revenue, COGS, Gross Profit, Operating Expenses, and EBITDA (Earnings Before Interest, Taxes, Depreciation, and Amortization).
  2. Cash flow measures covering cash inflows, outflows, and net cash
  3. Budgeted versus actual revenue figures
  4. Product-level revenue details and receivables aging information.
- A separate Date table was created to enable consistent time-based analysis and support accurate filtering by month, quarter, and year across all dashboard visuals.

## Key KPIs and Why They Matter:
- **1.	Total Revenue** (Formula Used: SUM(Data[Revenue]):
Measures overall business scale and growth for the selected period, helping stakeholders track performance trends and assess demand momentum.
- **2.	Net Cash** (Formula Used: SUM(Data[Cash Inflows])-SUM(Data[Cash Outflows])):
Represents the difference between total cash inflows and outflows, providing visibility into liquidity and the company’s ability to meet short-term obligations.
- **3.	Gross Profit %**(Formula Used: DIVIDE(SUM(Data[Gross Profit]), SUM(Data[Revenue]))):
Indicates operational efficiency and pricing effectiveness by showing how much revenue is retained after direct costs, enabling management to identify cost or pricing pressures.
- **4.	EBITDA %**(Formula Used: DIVIDE(SUM(Data[EBITDA]), SUM(Data[Revenue])):
Serves as a proxy for core operating profitability, independent of financing, tax, and accounting effects, supporting comparability over time and across scenarios.
- **5.	Budget Attainment %**(Formula Used:  DIVIDE(SUM(Data[Revenue]), SUM(Data[Revenue Budget])):
Measures how actual revenue compares to the planned budget for the selected period, calculated. This Chart helps stakeholders assess execution against plan, identify over- or under-performance early, and take corrective actions on pricing, costs, or investment priorities.
- **6.	Other DAX formulae Used are:**
    - **a.	Previous_Month_Rev** = CALCULATE(SUM(Data[Revenue]), DATEADD(Data[Month], -1, MONTH))
    - **b.	Operating_Cash_Flows** = SUM(Data[EBITDA])+SUM(Data[Cash Inflows])-SUM(Data[Cash Outflows])
    - All these measures were created using DAX measures to ensure correct aggregation and responsiveness to filters.

## Key Insights from the Dashboard:
- Revenue, Gross Profit & EBITDA Trends: Shows how topline growth translates into profitability over time, helping stakeholders identify margin expansion, compression, and periods of volatility. According to Dashboard, Revenue is around 24 million, Gross Profit is around 45.55 % and EBITDA is 24.81%.
- Budget vs. Actual Revenue: Compares planned versus realized revenue monthly, enabling early identification of over- or under-performance and timely corrective actions. According to dashboard, Several months show actuals marginally below budget, suggesting pockets of underperformance that may require targeted corrective actions (e.g., pricing, sales focus, or demand stimulation).
- Product Performance Analysis: Highlights revenue contribution by product or service, clearly distinguishing top-performing offerings from underperformers and informing portfolio and pricing decisions. Product C generates the highest revenue.
- Cash Flow Analysis: Tracks monthly cash inflows, outflows, and net cash to assess liquidity trends, cash sustainability, and potential funding risks. According to Dashboard, Cash inflows consistently exceed cash outflows across most months, resulting in a positive net cash position and indicating healthy underlying cash generation.
- Receivables Aging Analysis: Segments outstanding receivables into aging buckets to surface collection risks, support credit control actions, and improve working capital management.

## Conclusion:
- The financial dashboard delivers a consolidated, interactive view of the company’s overall financial health at a monthly level.
- It enables stakeholders to track performance trends, compare actual results against budget, and monitor profitability and cash flow dynamics.
- By highlighting variances, liquidity patterns, and potential risk areas, the dashboard supports informed, timely, and data-driven decision-making across the organization.
