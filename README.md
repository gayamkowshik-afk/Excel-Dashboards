# Excel Dashboards Portfolio

A collection of 4 interactive Excel dashboards, each built end-to-end inside a single workbook using PivotTables, PivotCharts, and slicers. Every workbook follows the same 3-stage structure:

1. **Data** — the raw dataset
2. **Analysis** — PivotTables that summarize the raw data (totals, breakdowns, trends)
3. **Dashboard** — PivotCharts and KPI cards built on top of the Analysis sheet, arranged into a single visual report

| # | Dashboard | File | Domain |
|---|-----------|------|--------|
| 1 | [HR Attrition Dashboard](#1-hr-attrition-dashboard) | `HR_DATA_Excel.xlsx` | Human Resources |
| 2 | [IPL Dashboard](#2-ipl-dashboard) | `IPL_DASHBOARD.xlsx` | Sports Analytics |
| 3 | [E-commerce Sales Dashboard](#3-e-commerce-sales-dashboard) | `Ecommerce_Sales_Analysis.xlsx` | Retail / Sales |
| 4 | [Swiggy Orders Dashboard](#4-swiggy-orders-dashboard) | `Swiggy_Raw_Data_Excel.xlsx` | Food Delivery |

---

## 1. HR Attrition Dashboard

**File:** `HR_DATA_Excel.xlsx`

Analyzes employee attrition across a company of 1,470 employees to identify which departments, age groups, and education levels are most affected.

**Sheets**
| Sheet | Contents |
|---|---|
| `Data` | Raw HR records — 1,470 rows × 44 columns (Department, Age, Job Role, Monthly Income, Job/Environment/Relationship Satisfaction, Work-Life Balance, Years at Company, Attrition flag, etc.) |
| `Analysis` | PivotTables summarizing headcount, attrition rate, and satisfaction scores by Department, Education, Age Band, and Gender |
| `Dashboard` | KPI cards + 9 PivotCharts |

**Dashboard visuals**
- KPI cards: Total Employees, Attrition Count, Attrition Rate, Average Age, Active Employees
- Attrition by Gender (donut)
- Attrition by Department (bar) — R&D and Sales drive most attrition
- Attrition by Education Field (bar)
- Attrition by Age Band (bar) — 25-34 age group has the highest attrition
- Job Satisfaction score (donut/gauge)
- Gender headcount split

**Key insight:** Attrition rate is ~16.1%, concentrated in the R&D and Sales departments and the 25-34 age band.

---

## 2. IPL Dashboard

**File:** `IPL_DASHBOARD.xlsx`

Explores 17 seasons (2008–2024) of IPL cricket match data — toss decisions, venues, winners, and Player-of-the-Match awards.

**Sheets**
| Sheet | Contents |
|---|---|
| `Matches` | Raw match-level data — 1,095 matches × 20 columns (Season, Date, Venue, Teams, Toss Winner/Decision, Match Winner, Result Margin, Umpires, etc.) |
| `Winning Data` | Season-by-season summary of Champion, Runner-up, and Player of the Series (2008–2024) |
| `Analysis` | PivotTables on toss decisions vs. wins, venue-wise match counts, and Player-of-the-Match award counts |
| `Dashboard` | 5 PivotCharts + a Title Winners chart |

**Dashboard visuals**
- Matches Won by Team — split by Bat-first vs. Field-first toss decision (bar)
- Toss Decision based Winning % (donut) — teams that chose to field after winning the toss won more often
- Top 10 Venues by match count, broken down by toss decision (bar)
- Top 10 Player-of-the-Match award winners (bar)
- Title Winners across seasons (chart built on the `Winning Data` sheet)

**Key insight:** Fielding first after winning the toss has historically been the more successful strategy across most IPL venues.

---

## 3. E-commerce Sales Dashboard

**File:** `Ecommerce_Sales_Analysis.xlsx`

A retail sales & profitability dashboard built on ~10,000 order line items (Superstore-style dataset), spanning Furniture, Office Supplies, and Technology categories.

**Sheets**
| Sheet | Contents |
|---|---|
| `Data` | Raw order data — 9,994 rows × 22 columns (Order ID, Order/Ship Date, Customer, Segment, Region, Category, Sub-Category, Sales, Quantity, Discount, Profit) |
| `Analysis` | PivotTables for monthly Sales/Profit/Quantity/Order Count/Profit Margin trends, plus Category and Sub-Category breakdowns |
| `Dashboard` | 10 PivotCharts |

**Dashboard visuals**
- Monthly Sales trend (line)
- Monthly Profit trend (line)
- Monthly Quantity Sold trend (line)
- Monthly Order Count trend (line)
- Monthly Profit Margin trend (line)
- Sales by Category — Furniture / Office Supplies / Technology (donut)
- Sales by Sub-Category, e.g. Binders, Tables, Storage, Chairs, Phones (bar)
- Combined Sales vs. Profit comparison chart (area + bar)

**Key insight:** Sales peak in Nov–Dec (holiday season), with Technology as the strongest-margin category; Phones and Chairs are the top-selling sub-categories.

---

## 4. Swiggy Orders Dashboard

**File:** `Swiggy_Raw_Data_Excel.xlsx`

A food-delivery order analysis covering ~197,000 Swiggy orders across multiple Indian cities, restaurants, and dish categories.

**Sheets**
| Sheet | Contents |
|---|---|
| `Swiggy Data` | Raw order-level data — 197,430 rows × 14 columns (State, City, Order Date, Day, Quarter, Week, Restaurant Name, Location, Category, Dish Name, Food Type, Price, Rating, Rating Count) |
| `analysis` | PivotTables for KPIs, Veg/Non-Veg split, daily/weekly/monthly sales trends, and Top 5 Cities by sales |
| `DASHBOARD` | KPI cards + 6 PivotCharts |

**Dashboard visuals**
- KPI cards: Total Sales (₹53M), Total Orders (197,430), Average Rating (4.34), Average Order Value (₹268.5)
- Veg vs. Non-Veg sales split (donut) — Veg dishes account for ~63% of sales
- Daily Sales Trend by day of week (line)
- Weekly Sales Trend (bar)
- Monthly Sales Trend, Jan–Aug (bar)
- Top 5 Cities by Sales (bar) — Bengaluru leads, followed by Lucknow, Hyderabad, Mumbai, and New Delhi

---

## How each dashboard was built

All 4 workbooks follow the same workflow:

1. **Data** — raw, unmodified source data sits in its own sheet.
2. **Analysis** — PivotTables reference the Data sheet to compute aggregates (sums, counts, averages) grouped by the relevant dimensions (time, category, department, etc.).
3. **Dashboard** — PivotCharts and KPI text boxes are built on top of the Analysis sheet's PivotTables, with slicers added for interactive filtering, then laid out together into a single-page report.

## Tools used
- Microsoft Excel
- PivotTables & PivotCharts
- Slicers (for interactive filtering)

## Repository structure
```
├── HR_DATA_Excel.xlsx
├── IPL_DASHBOARD.xlsx
├── Ecommerce_Sales_Analysis.xlsx
├── Swiggy_Raw_Data_Excel.xlsx
└── README.md
```

## How to use
1. Download/clone the repo.
2. Open any workbook in Excel.
3. Go to the `Dashboard` (or `DASHBOARD`) sheet to view the interactive report.
4. Use the slicers to filter by category, region, season, etc.
5. Check the `Data` and `Analysis` sheets to see how each chart's numbers are derived.
