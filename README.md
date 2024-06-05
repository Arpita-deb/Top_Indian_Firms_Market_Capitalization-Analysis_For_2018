# Charting Progress: An examination of Market Capitalization in the Indian Corporate landscape in 2018
## Unified Mentor Internship Project 1: Financial Analytics

![Financial Analysis presentation](https://github.com/Arpita-deb/Top_Indian_Firms_Market_Capitalization-Analysis_For_2018/assets/139372731/b2b9a4cc-9725-43a6-81b6-bc65f89fc1de)

# About the Internship:

* Organization: Unified Mentor
* Role: Data Analyst Intern
* Timeline: 10-05-2024 to 10-06-2024
* Number of Projects: 2
* Project Names: Financial Analytics & Budget Sales Analytics

# About the Project:

## Project Name: 
 - Financial Analytics

## Introduction:
 - To ensure business sustainability and growth, it is imperative to conduct a thorough analysis of market competition. This assignment involves examining the competitive landscape to enhance the strategic positioning and performance.
   Using data about market capitalization details of India’s top 500 firms for FY 2018, I have to derive insights that can inform management decisions. My toolkit includes Excel, Alteryx, Power BI, Google Slides, and Canva. Market Capitalization served as my primary metric to gauge corporate competitiveness. I’ve also discussed the project’s limitations and proposed some future directions.

   The Project Report is available here [Financial Analysis Report Presentation PDF](https://github.com/user-attachments/files/15572726/Financial.Analysis.Report.Presentation.pdf).

## Domain: 
 - Finance

## Difficulty Level: 
 - Intermediate

## Problem Statement: 
- I am tasked to analyse the market competition for the management of 500 companies in India for Financial Year 2018 to provide better results and insights.

## Deliverables:
  - Datasets used
  - Alteryx Workflows
  - Project Report (Presentation)
  - Power BI Dashboard
  - GitHub Documentation

## Tools used:
  - Microsoft Excel - For Initial Data Cleaning (Removing Typographical errors)
  - Alteryx - For Data Preparation, Joining external dataset, Exploratory Data Analysis (EDA)
  - Power BI - For Data Visualization
  - Canva - For Project Report

## Methodologies used:
  - Data Profiling
  - Data Cleaning
  - Data Wrangling
  - Exploratory Data Analysis
  - Data Visualization
  - Documentation

## Data Description:

1. **[Finance Data](https://www.kaggle.com/datasets/nishankmagoo/top-500-companies-in-india) - Data on Fortune 500 Companies in India**

| Column name | Datatype | Type | Description |
| :--- | :--- | :--- | :--- |
| S.No. | integer | NON NULLABLE| Index of the rows |
| Name | string | NON NULLABLE | Name of the Companies |
| Mar Cap - Crore | double | NON NULLABLE | Market Capitalization for each company in Crores |
| Sales Qtr - Crore | double | NON NULLABLE | Quarterly Sales for each company in Crores |

2. **[NIFTY 500 Stats](https://www.kaggle.com/datasets/dhimananubhav/nifty-500-fundamental-statistics) - Data on top 500 companies in India's National Stock Exchange (NSE) based on market capitalisation and average daily turnover.**

| Column name | Datatype | Type | Description |
| :--- | :--- | :--- | :--- |
| index | integer | NON NULLABLE| Index of the rows |
| company | string | NULLABLE | Name of the Company |
| industry | string | NULLABLE | Sector of operation |
| symbol | string | NULLABLE | Ticker |
| category | string | NULLABLE| Nifty 50, Nifty Next 50, Nifty Midcap 150 and Nifty Smallcap 250 |
| market_cap | double | NON NULLABLE | Market capitalization in INR Crore |
| current_value | double | NON NULLABLE | Latest stock value |
| high_52week | double | NON NULLABLE | 52 week high |
| low_52week | double | NON NULLABLE| 52 week low |
| book_value | double | NON NULLABLE | Book value |
| price_earnings | double | NON NULLABLE | P/E ratio |
| dividend_yield | double | NON NULLABLE | Dividend yield % |
| roce | double | NON NULLABLE | Return on capital employed % |
| roe | double | NON NULLABLE | Return on equity % |
| sales_growth_3yr | double | NON NULLABLE | Average 3 year sales growth % |

## Limitation of the dataset:

1. One major limitation in the dataset provided is that it doesn't contain 500 companies.
2. The market capitalization data varies for the year 2018 in various other datasets containing the fortune 500 Indian companies list.
3. The dataset doesn't include many other quantitative and qualitative columns which limits the insights that could have been generated.
4. 'Sales Qtr - Crore' column is ambiguous.

To address the third issue, I used another external dataset names 'NIFTY 500' from Kaggle which I used to add the sector for each of these companies.

## Key Performance Indicators (KPIs) to measure:

1. **Market Capitalization**: Market capitalization, often referred to as "market cap," is the total value of a company's outstanding shares of stock.
	
       Market Capitalization = Price Per Share × Shares Outstanding

2. **Quarterly Sales**: Quarterly revenue growth measures the increase in a firm's sales from one quarter to another.

3. **Rank**: Rank of a company based on their total market cap in 2018. This is calculated by Sorting the companies by Market Cap in descending order and indexing them starting from 1. So the company with highest market cap will rank 1, the second highest 2 and so on.

4. **Market Share**: It is the percentage of total sales in an industry generated by a particular company. It gives a general idea of the size of a company in relation to its market and competitors.

       Market Share = Company's Quarterly Sales/Total Quarterly Sales of All Companies * 100

5. **Sales Yield**:  In the context of a company's market capitalization, the sales yield metric can be interpreted as the **Market Cap to Sales Ratio**. This ratio is used to determine how much price investors are willing to pay for every unit of a company's sales. 

       Sales Yield = Market Capitalization/Total Sales
  
## Data Cleaning:

   I used Microsoft Excel and Alteryx for cleaning and transforming the data. In this phase I removed duplicate entries, corrected typographical errors, joined column from external dataset, organized the data by sorting and filtering, created numerical and categorical columns based on existing one. I've documented all the changes here in this [Changelog](https://docs.google.com/document/d/1lDhmjGJxXsieriydLpLRMFHGMSKQQsCbhuTJqJbyLkw/edit?usp=sharing).

  After cleaning and transforming the dataset, we end up with 9 columns and 487 rows -

  | Column name | Datatype | Type | Description |
  | :--- | :--- | :--- | :--- |
  | Rank | integer | NON NULLABLE | Ranking based on Market Capitalization for each company |
  | CompanyID | integer | NON NULLABLE | Unique id for each company |
  | Company Name | string | NON NULLABLE | Name of the Company |
  | Market Capitalization (in Crore) | double | NON NULLABLE | Market Capitalization for each company in Crores INR |
  | Quarterly Sales (in Crore) | double | NON NULLABLE | Quarterly Sales for each company in Crores INR |
  | Industry | string | NON NULLABLE | Sector of operation |
  | Market Share | double | NON NULLABLE | % of total sales generated |
  | Sales Yield | double | NON NULLABLE | Return on Investment |
  | Category | string | NON NULLABLE | Category based on Market Cap(Small, Mid, Large) |

## Data Exploration:

  I explored the data to understand its characteristics and patterns using Alteryx and Microsoft Power BI. It involved using descriptive statistics and data visualization techniques. Here I answered the following questions-

![A 1 1](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/a9e84719-c9b8-4125-a9f6-9226b5006811)

![A 1 1 2](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/6192bcdf-ef01-4180-a639-cf050450d37c)

![A 1 2](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/8ffb3a6a-a705-4d2c-b4a6-1e53ac0f550d)

![1 3](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/125925df-11bb-49fc-a15b-21b1559fce3e)

![A 1 4](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/46f566b5-1c47-4b7f-86ae-3e8fb579c44b)

![A 1 5](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/87f14a4f-e148-4221-be18-4f6427da592c)

![A 1 6](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/31e28f34-6494-40ca-bb44-9608329fe3b4)

![Boxplot](https://github.com/Arpita-deb/netflix-movies-and-tv-shows/assets/139372731/8a4b7889-595d-4503-a3db-c56661efc2ed)

![A 1 7](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/53c8bb6b-7497-4869-80bf-e43286a08217)

![A 1 8](https://github.com/Arpita-deb/netflix-movies-and-tv-shows/assets/139372731/e679db35-f611-402c-a37d-4e2818d747a2)

![A 1 9 1](https://github.com/Arpita-deb/netflix-movies-and-tv-shows/assets/139372731/ce1a8919-01b3-4b6a-a346-d1f61b3f89b7)

![A 1 9 2](https://github.com/Arpita-deb/netflix-movies-and-tv-shows/assets/139372731/0faf7415-61b9-45c4-b5ad-d3cd7030c415)

![A 1 10 2](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/aba5bdd1-d784-4587-9a36-4eced5fb188e)

![A 1 10 2](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/a38c4847-f765-4f6c-b7cc-96600a11ed9b)

* **Summary of Exploratory Data Analysis:**

1. The analysis reveals outliers in Quarterly Sales and Market Capitalization among 487 companies. The median market cap is ₹28,784 crore, with the highest at ₹5,83,436 crore, indicating significant variance. The top three companies by market cap in 2018 were *Reliance Industries, Tata Consultancy Services*, and *HDFC Bank*, holding market shares of 32.85%, 31.74%, and 27.19%, respectively.

![Top 15 companies](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/e604815e-a27f-4ca8-bf9e-d5edc870ee3f)

2. The *IT, Energy*, and *Metals* sectors led in Average Market Capitalization. Notable outliers included Reliance Industries from Energy and Tata Consultancy Services from IT.

![Industries](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/19d28b41-d60c-41b8-a4f2-630f6d753c1c)

3. Market capitalization correlated moderately with sales, with a coefficient of 0.5868. Companies were classified into large (market cap > ₹28,000 crore), mid (market cap between ₹8,000 crore and ₹28,000 crore), and small (market cap < ₹8,000 crore) categories, with small caps being the majority.

![donut](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/03865a68-a000-46e8-9af1-6dbf86fcd3eb)

4. A Further breakdown of total Market Share by industries and categories reveal that the top performing industries were dominated by Large Cap Companies, which also answers their high market share. However, there are some emerging industries dominated by Mid and Small Cap companies which reveals potential for these small and mid cap companies to emerge and thrive.

![stack](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/9a9b0f2d-f339-4641-bf67-f1311013251c)

5. A scatterplot comparing Quarterly Sales and Market Cap ranks showed minimal positive correlation, with only 31 companies ranking under 50 in both categories. This gets more complicated as we've ranked the companies in descending order of their market cap and sales, which means companies ranking higher in market cap (i.e. closer to 1) also have a higher sales rank (i.e. closer to 1). This means that as the rank of a company by market cap increases there tends to be a tendency for its rank by quarterly sales to also increase.

However, correlation does not imply causation. This means that while there is a relationship between market cap ranks and quarterly sales ranks, it doesn't necessarily mean that one directly causes another. Other factors could influence both market cap and sales independently.

![scatter](https://github.com/Arpita-deb/Unified-Mentor-Internship-Project-Works/assets/139372731/650a61f2-9f75-4dd7-b9c5-6318a1766e84)  

## Interpretation of Results:
1. **Market Capitalization Metrics:**
   - Market capitalization is a crucial metric for assessing a company's competitiveness. We grouped companies into three distinct categories based on their market cap. Approximately 21% of all companies fall into large cap category, with a market cap exceeding ₹28,000 Crore INR. Reliance Industries Ltd, Tata Consultancy Limited, and HDFC Bank lead the way, generating over ₹16,00,000 Crore in market capitalization. Larger market caps often indicate a company's ability to influence the market, attract investors, and fund operations.

2. **Market Share Insights:**
   - In the Indian business landscape of 2018, companies like Reliance Ltd and Tata Consultancy Group held significant market share. High market share suggests market leadership, a strong brand, and considerable influence over prices and trends. Markets with a few dominant players are less competitive, while those with many smaller players are more competitive.

3. **Industry-Specific Analysis:**
   - In 2018, IT, Energy, Automobile, Metal, Telecom, and Logistics industries stood out. These sectors were predominantly monopolized by large and mid-cap companies.

4. **Emerging Small Caps:**
   - Despite the dominance of large and mid-cap companies, 46% of analyzed firms were Small Caps. Industries like Agriculture, Paper, Healthcare, Textile, Services, Construction, and Chemicals show promising growth.

## Limitations of the project:

1. The dataset was incomplete with only 488 rows with 1 duplicate entry instead of 500.
2. The ambiguous nature of Quarterly Sales column restricted further calculation.
3. The data did not contain other numeric columns such as Revenue, Quarterly sales for different quarters, Market cap from previous years etc which could have allowed us to perform more advanced analysis such as Sales Efficiency Analysis, Growth Analysis, Correlation and Regression Analysis, Predictive Analysis etc.
4. Since the data is not normally distributed, I could not perform Hypothesis Test (ANOVA) to check whether there was any affect of Industry in Market Capitalization.

## Future Ideas:

1. In order to analyze competition among companies one can collect these data -

   - Market Research Data including information about industries,market trends, customer preferences and demographics.
   - Financial statement such as income, balance sheets, cash flow statements to provide insights into a company's profitability, liquidity and financial health.
   - Market Share Data within specific sector or region.
   - Details about products and services offered by each competitor, including pricing strategies, product features and customer value propositions.
   - Customer data including customer behavior, satisfaction levels and loyalty.
   - Marketing and sales strategies, distribution campaigns, sales tactics and promotional activities to understand how competitors attract and retain customers. 

2. Compare various metrics such as revenue, profit margins, return on investment (ROI), debt levels across competitors to reveal strengths and weaknesses.

3. Perform more advanced data analysis techniques e.g., -
   - Correlation Analysis - to help undestand relation between two or more variables.
   - Regression Analysis - to predict one or more independent variables (e.g., pricing, promotion efforts) on a dependent variable (e.g., sales revenue, market share etc).
   - Cluster Analysis - to group competitors based on similar attributes such as market segments, product features or customer demographics.
   - Trend Analysis - to assess sales growth rates, market share changes etc to identify emerging trends and opportunities.
   - SWOT Analysis -  to systematically evaluate internal and external factors affecting competitiveness.

## References:

* Datasets used:
  - [Top 500 Companies in India](https://www.kaggle.com/datasets/nishankmagoo/top-500-companies-in-india)
  - [ET Top 500 Indian Companies (2009-2021)](https://www.kaggle.com/datasets/ramjasmaurya/et-top-500-indian-companies-since-2009)
  - [Nifty 500 fundamental statistics](https://www.kaggle.com/datasets/dhimananubhav/nifty-500-fundamental-statistics)
* [Market Capitalization - Basics, Definition, How to Calculate](https://groww.in/p/market-capitalisation)
* [Market Capitalization Basics: Large cap, Mid cap & Small cap companies](https://tradebrains.in/market-capitalization-in-indian-stock-market/)
* [Market Cap To Sales Ratio: Why It's Important? - StockEdge Blog](https://blog.stockedge.com/market-cap-to-sales-ratio/)
