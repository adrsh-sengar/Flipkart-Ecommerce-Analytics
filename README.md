# Flipkart Big Billion Days — E-Commerce Analytics Dashboard

Flipkart's Big Billion Days is one of the biggest sales events in Indian e-commerce. Massive revenue numbers look great on paper — but when you dig into the data, aggressive discounting can quietly destroy profitability. This project is about finding exactly that.

---

## The Problem

During Big Billion Days, Flipkart offers heavy discounts across thousands of product categories to drive volume. The business question nobody was answering clearly was — **are we actually making money, or just moving products?**

With no category-level visibility into discount ROI, finance teams couldn't tell which categories were profitable, which were bleeding margin, and whether the overall sale was hitting its targets. This project builds that visibility.

---

## What I Found

Despite generating **$431.5K in total revenue**, aggressive discounting diluted the net profit margin to just **5.55%** ($23.96K net profit) — roughly **50% below** the finance team's target.

That's the kind of insight that changes how a business thinks about its next sale.

---

## Dashboard Preview

![image](https://github.com/adrsh-sengar/Flipkart-Ecommerce-Analytics/blob/main/Final_Dashboard/Fliplart_Dashboard.pdf)

---

## Tools Used

- **Python (Pandas)** — data cleaning, validation, and anomaly detection on raw transactional data
- **Power BI** — multi-page interactive dashboard with Star Schema data model and DAX measures
- **MS Excel** — raw data source (CSV files)

---

## How It Works

**Step 1 — Data Cleaning**
The raw CSV files had inconsistencies, missing values, and anomalies. Python (Pandas) was used to clean and validate the data before any analysis — garbage in, garbage out applies here more than anywhere else.

**Step 2 — Data Modelling (Star Schema)**
To ensure accurate DAX calculations and dynamic filtering without relationship conflicts, the data was structured into a strict Star Schema:
- **Fact Tables:** Order Details (transactions) and Sales Target (goals)
- **Dimension Tables:** Geographic data, Category bridge table, and a custom DAX-generated Calendar table for unbroken time-series analysis

**Step 3 — Dashboard**
Power BI dashboard built across multiple pages covering:
- Revenue vs. target tracking
- Profit margin by category
- Discount impact analysis
- Geographic sales performance
- Time-series trend analysis

DAX measures handle all dynamic KPI calculations — profit margin %, discount rate, revenue gap from target — all responding to slicer selections in real time.

---

## Key Findings

- Net profit margin of **5.55%** on $431.5K revenue — roughly half of what the finance team targeted
- Identified which product categories had the worst discount-to-margin ratio — these are the ones dragging overall profitability down
- Geographic breakdown revealed which regions were driving volume vs. which were actually profitable
- Time-series analysis showed which days of the sale had the highest revenue leakage due to over-discounting

---

## What I Learned

The most interesting part of this project wasn't building the dashboard — it was realising how easy it is for a business to confuse revenue with profit. Big Billion Days looks like a massive success from a GMV perspective. But once you break it down by category and factor in discounts, the picture gets a lot more complicated.

The Star Schema modelling was also a good exercise in thinking about data relationships before touching Power BI — getting the model right upfront saved a lot of headache with DAX calculations later.

---

## File Structure

```
├── Raw_Data.csv                    # Original dataset
├── Python_EDA.py                   # Data cleaning and anomaly detection
├── Flipkart_Command_Center.pbix    # Power BI dashboard file
├── Dashboard_Report.pdf            # Static snapshot of dashboard views
├── images/                         # Dashboard screenshots
└── README.md
```
