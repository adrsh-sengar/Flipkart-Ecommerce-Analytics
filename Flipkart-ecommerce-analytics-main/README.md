
https://github.com/user-attachments/assets/137d9e21-aab5-41c0-a283-06946d2d1ea7
Uploading Dashboard_demo.mp4…
# 🛒 Flipkart Big Billion Days: Post-Sale Analytics Hub

## 📌 Project Overview
The "Big Billion Days" is a massive e-commerce event, but high Gross Merchandise Value (GMV) often masks shrinking profit margins due to heavy discounting. I built this **End-to-End Enterprise Command Center** to give C-suite executives a clear, actionable post-sale autopsy. 

Instead of just tracking vanity metrics, this tool uncovers regional losses, highly profitable sub-categories, and critical data engineering flaws.

### 📂 Files Included in this Repository
* **`Flipkart_Command_Center.pbix`**: The fully interactive Power BI dashboard.
* **`Dashboard_Demo.mp4`**: A video walkthrough of the interactive UI/UX and cross-filtering features.
* **`Dashboard_Report.pdf`**: Static snapshot of the executive views.
* **`Python_EDA.py`**: The Python script used for initial data cleaning and anomaly detection.
* **`Raw_Data.csv`**: The initial dataset used for modeling.

---

## 🛠️ Tech Stack & Skills Demonstrated
* **Exploratory Data Analysis (EDA):** Python (Pandas)
* **Data Engineering:** Power Query, Star Schema Data Modeling
* **Business Logic:** Advanced DAX (Time Intelligence, Dynamic Targets, Margin Ratios)
* **UI/UX Design:** Power BI (Custom layouts, cognitive load reduction, brand alignment)

## 🏗️ Data Architecture (The Star Schema)
To ensure dynamic filtering and accurate DAX calculations without relationship loops, I modeled the raw CSV files into a strict Star Schema:
* **Fact Tables:** `Order_Details` (Transactions) and `Sales_target` (Goals).
* **Dimension Tables:** `List_of_Orders` (Geographic data), `Category_Dim` (Bridge table), and a custom DAX-generated `Calendar` table for unbroken time-series analysis.

---

## 📊 Key Executive Insights

### 1. The Target Miss & Tight Margins
Despite generating **$431.5K** in total revenue, aggressive discounting diluted the profit margin to just **5.55%** ($23.96K Net Profit), only hitting ~50% of the finance team's target.

### 2. The "Hero" vs. "Villain" Products
* **Heroes:** Printers ($6.0K) and Bookcases ($4.9K) acted as the core profit engines.
* **Villains:** The Furniture category (specifically Tables) operated at a massive **-$4.0K loss**. Selling more tables during this event actively hurt the company's bottom line.

### 3. Geographic Bleed
Northern hubs like Uttar Pradesh ($2.8K) and Delhi ($2.2K) are highly profitable, but the Southern markets (Tamil Nadu, Andhra Pradesh) are operating at a severe net loss, requiring an immediate logistics review.

### 4. 🚨 Critical Data Quality Catch
During EDA, I discovered that **89% of profitable orders lacked geolocation data** (Categorized as "Blank"). This indicates a critical failure in the CRM/Checkout data capture process that requires immediate engineering intervention.

---

## 🎨 UI/UX Design Approach
Designed with **Executive Cognitive Load** in mind:
* Strict adherence to Flipkart brand guidelines (High-contrast Yellow/Blue).
* Soft drop-shadows and rounded borders to mimic a modern web-application interface.
* Optimized "Data-to-Ink" ratio by removing redundant axes and gridlines.
* Custom page navigation built directly into the header ribbon.
