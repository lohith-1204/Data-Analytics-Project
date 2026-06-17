# Data Analytics Project

A multi-tool data analytics portfolio covering SQL, Python, Excel, Big Data (Hive), and BI dashboarding (Tableau/Power BI–style visuals). The repo is organized as a flat collection of standalone projects rather than nested folders, with each file (or small group of files) representing a self-contained exercise in a particular tool.

## SQL

**[SQL - Data Cleaning.sql](./SQL%20-%20Data%20Cleaning.sql)** — Cleans a Nashville housing dataset: standardizes date formats, fills missing property addresses via self-joins, splits address fields into street/city/state using a custom `SPLIT_STR` function, normalizes Y/N flags into Yes/No, removes duplicates with a windowed CTE, and drops unused columns.

**[SQL - Data Exploration.sql](./SQL%20-%20Data%20Exploration.sql)** — Explores global COVID-19 case and vaccination data: death/infection rates by country and continent, global daily totals, and rolling vaccination percentages using window functions, CTEs, a temporary table, and a view for downstream visualization.

**[Instagram Clone SQL - Database & Inserting Data.sql](./Instagram%20Clone%20SQL%20-%20Database%20%26%20Inserting%20Data.sql)** — Builds a relational schema for an Instagram-style app (`users`, `photos`, `comments`, `likes`, `follows`, `tags`, `photo_tags`) and seeds it with data.

**[Instagram Clone SQL - Exploratory Data Analysis.sql](./Instagram%20Clone%20SQL%20-%20Exploratory%20Data%20Analysis.sql)** — Eighteen analysis questions against that schema (most active users, top hashtags by usage and likes, registration trends by day of week, regex-based username filtering, engagement and comment-rate breakdowns) plus four stored procedures for popular tags, engaged users, comment counts, and per-user activity lookup.

**[PostgreSQL-BI-CHALLENGE](./PostgreSQL-BI-CHALLENGE)** — A three-part business intelligence case study on a construction bidding platform (projects, bid packages, bid requests, subcontractors): data quality checks (duplicates, nulls), analysis of bid request volume, conversion rates, and decline reasons by subcontractor type, and a closing segmentation of subcontractors by country.

## Python

**[Python - Movie Industry EDA Project.ipynb](./Python%20-%20Movie%20Industry%20EDA%20Project.ipynb)** — An exploratory analysis of the film industry using pandas, matplotlib, and seaborn, framed as a business case for a company entering the movie business. It works through eight questions — optimal production budget, most profitable genres, best release timing, highest-value actors/directors, Oscar-winning budget thresholds, the effect of rating/runtime, profitability benchmarks against major studios, and which studio to model best practices on — and closes with a numbered set of actionable recommendations.

## Hadoop / Hive

**[Hadoop(Hive) - NYC Yellow Taxi Case Study.txt](./Hadoop(Hive)%20-%20NYC%20Yellow%20Taxi%20Case%20Study.txt)** — HiveQL queries against NYC Yellow Taxi trip data: table creation and load, total trips and revenue, toll/tip share of revenue, average fare by payment type, highest-revenue hour of day, and average trip distance.

## Excel

| File | Sheets / focus |
|---|---|
| [Excel - LOOKUP, INDEX, MATCH, SUMIFS.xlsx](<./Excel - LOOKUP, INDEX, MATCH, SUMIFS.xlsx>) | A customer quoting workbook using `LOOKUP`/`INDEX`/`MATCH` against an international price list and a `SUMIFS`-driven discount matrix. |
| [Excel - Pivot Tables, Pivot Chart, Slicers.xlsx](<./Excel - Pivot Tables, Pivot Chart, Slicers.xlsx>) | Shipping data summarized with pivot tables, a pivot chart, and slicers, with per-rep breakdown sheets. |
| [Excel - Sales Performance Dashboard.xlsx](<./Excel - Sales Performance Dashboard.xlsx>) | A sales dataset rolled up into trend, region, product, segmentation, and state views, combined into a single dashboard sheet. |
| [Excel - Scenario Manager, Solver (Data Modeling).xlsx](<./Excel - Scenario Manager, Solver (Data Modeling).xlsx>) | A project costing model with Scenario Manager and Solver used for what-if analysis and optimization. |

Screenshots of each workbook's output are in [`visuals/excel/`](./visuals/excel).

## BI Dashboards

Static exports of dashboards built in Tableau/Power BI-style tools, in [`visuals/`](./visuals) (with two duplicated at the repo root):

- **Instagram Clone Data Analysis Dashboard** — visual layer on top of the Instagram Clone SQL data: most-liked users, most active posters, sign-ins by day, and most-used hashtags.
- **SuperStore Weekly series** (`TopDownDashboard`, `BottomUpDashboard`, `KPIDashboard`, `Q&ADashboard`, `GeoChart`) — five linked dashboards over the same retail superstore dataset, each built from a different design approach (top-down KPI view, bottom-up exploratory view, executive KPI scorecard, guided Q&A view, and a geographic customer map).
- **Retail Pricing Analytics** — profit and pricing-curve analysis to find the price point that maximizes profit across product lines.
- **London Bus Safety** — incident counts by borough, type, route, and season for London buses (2015–2018).
- **E-Commerce Retail** — email campaign revenue, top cities by sales, and traffic-source breakdown for an online store.
- **World Bank CO2 Emission** — CO2 emissions and per-capita emissions by country over time, using World Bank data.
- **Work From Home** — a Makeover Monday-style breakdown of why people prefer remote work.
- **Municipality Data Analysis Dashboard** and **Grover Data Analyst Dashboard** — case-study dashboards on social media post volume by category/source and on order/revenue trends, respectively.

## Tech stack

- **SQL:** MySQL-flavored SQL (window functions, CTEs, views, stored procedures, regex), PostgreSQL
- **Python:** pandas, numpy, matplotlib, seaborn
- **Big Data:** Apache Hive (HiveQL)
- **Spreadsheets:** Excel (LOOKUP/INDEX/MATCH, SUMIFS, PivotTables, Slicers, Scenario Manager, Solver)
- **BI/Visualization:** Tableau-style dashboarding

## Notes

- The `.sql` files are scripts meant to be read or run against a database with the referenced tables already loaded (e.g. `nashville_housing`, `coviddeaths_csv`, `covidvacinations_csv`) — the underlying datasets aren't included in this repo.
- The Hive case study is a plain-text walkthrough of queries and tasks rather than a runnable script.
- Some dashboards in `visuals/` are practice/case-study exercises (credited to their original designer where the image itself carries that credit) rather than dashboards built from scratch on original data; they're included here as part of the BI skills on display.
