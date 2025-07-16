# 📚TABLE OF CONTENTS
- [🧋 INTRO](#intro)
- [1️⃣ Final Summary worksheet](#1_final-summary-worksheet)
- [2️⃣ Missed Order worksheet](#2_missed-order-worksheet)
- [3️⃣ Customer Report worksheet](#3_customer-report-worksheet)
- [4️⃣ Pivot Analysis worksheet](#4_pivot-worksheet)
- [📌 CONCLUSIONS](#conclusions)

---

# 🧋INTRO
- **INTERMEDIATE EXCEL:** `3D formulas`, `nested functions`, `sparklines`, `conditional formatting`, `pivot tables/charts/slicers`, and `forecasting`.

## Resources
👉 Click HERE: [Intermediate_Excel_boba](https://github.com/amy941/boba_data_crunch/blob/main/1_Excel_Intermediate_boba/Intermediate_BubbleTea_project.xlsx)

👉 Click HERE: [raw_data](https://github.com/amy941/boba_data_crunch/tree/main/raw_data/Intermediate_raw)

## Sheets Overview
This Excel includes **12 color-coded worksheets**, each serving a specific purpose:
  * **Orders Term 1–4:** Raw scores & ratings
  * **Final Summary:** Aggregated scores, grades, and insights
  * **PIVOT:** Grade breakdowns & forecasts
  * **Customer Report:** Cleaned names, emails, IDs, and trends
  * **Missed Orders + Missed Term 1–4:** Missed pickups summary
    
Color-coded tabs guide the workflow

---

# 📉1_FINAL SUMMARY worksheet
## 🔗Link: [Intermediate_Excel_boba](https://github.com/amy941/boba_data_crunch/blob/main/1_Excel_Intermediate_boba/Intermediate_BubbleTea_project.xlsx)

- **Purpose:** Customer feedback for barista performance across four terms and sugar/ice preferences.
- **Skills:** `3D-Formulas`, `Linking worksheets`, `Named Ranges`, `Text functions`

## ✨Hightlights
- **3D-formulas:** to calc. average scores across Term 1-4
    ```=AVERAGE('Orders Term 1:Orders Term 4'!E4)```
- **Name Ranges:** ```Create from Selection``` for clean, readable format.
- **COUNTIFS and Conditional Formatting** to track & highlight grade distribution.
      
## 🔎Key Insights

![final_sum](https://github.com/user-attachments/assets/241a05cd-f704-430d-ba27-0b16d2c5a0d0)

_Screenshot of the Final Summary worksheet showing performance grades, summary statistics, and sugar/ice preferences._

- Customer **Noah Chen** gave **Barista Amy** a top score of **91** (highlighted in RED)
- **Barista Amy** earned: 13 A's, 9 B's, and 0 C's
- **79 Bs grades** were received across all baristas
- Customers preferred **moderate sugar (40-60%)** and **light to moderate ice (25-50%)**



---

# 📉2_MISSED ORDER worksheet
## 🔗Link: [Intermediate_Excel_boba](https://github.com/amy941/boba_data_crunch/blob/main/1_Excel_Intermediate_boba/Intermediate_BubbleTea_project.xlsx)

- **Purpose:** Track customer no-shows by counting missed drink pickups across 4 terms.
- **Skills:** `Consolidation`, `Sort & Filter`, `Conditional Formatting`

## ✨Hightlights
- **Consolidation Tool** used to merge data from ```Missed Term 1``` to ```Missed Term 4```
- **Sorting** missed pickup from smallest to largest
- **Conditional Formatting** to highlight customers with **2+ missed orders.**
      
## 🔎Key Insights

![missed_order](https://github.com/user-attachments/assets/3f795e3c-e995-4255-a9fc-d28244c31773)

_Screenshot of the Missed Orders worksheet displaying consolidated no-show data across four terms, frequent absentees flagged in red._

- Most customers missed only **one pickup**
- **5 customers** missed **2 or more** drink pickups
- **CUST0079** is the highest no-show with **3 missed orders**

  
---

# 📉3_CUSTOMER REPORT worksheet
## 🔗Link: [Intermediate_Excel_boba](https://github.com/amy941/boba_data_crunch/blob/main/1_Excel_Intermediate_boba/Intermediate_BubbleTea_project.xlsx)

- **Purpose:** Transform raw customer data into a clean format and analyze individual barista performance.
- **Skills:** `Text functions`, `Nested formulas`, `Conditional functions`, `Sparklines`, `Structured Tables`

## ✨Hightlights

![customer_report_1](https://github.com/user-attachments/assets/61d457ab-7002-45f0-9e9e-bcce155ffee3)

_Screenshot of the Customer Report worksheet, showing "cleaned" customer records using Text functions._

- **Text Functions** to format data:
  * **Full Name** (e.g., Ava Hoang) ➡️ `=PROPER(CONCAT(B4," ",C4))`
    
  * **Email Address** (e.g., ahoang@bbt.com)  ➡️ `=LOWER(CONCAT(LEFT(B4,1),C4,"@bbt.com"))`
    
  * **ID tags** (e.g., 2015-001) ➡️ `=CONCAT(2015,"-",RIGHT(A4,3))`


---

![sparkline](https://github.com/user-attachments/assets/51da85e0-797b-4a5e-a58a-a5d0b3d55bb6)

_Screenshot of the Customer Report worksheet, showing performance trends over 4 terms._

- **Sparklines** to visualize how baristas have progressed over the year.
  * Use **High Point** markers to highlight performance peaks.
  * Example: Barista Tom's peak performance score is 86 in Term 3, graded by Liam Kim, visible in the orange dot.


---
![total_row](https://github.com/user-attachments/assets/32d8e656-85bf-4776-8a08-22a89d8028e4)

_Screenshot of the Customer Report worksheet, showing missed orders and total fees in structured tables._

- **Structured Table** with ```Total Row``` enabled:
  * Average Performance Final Score: **91**
  * Total Missed Orders: **100**
  * Total Fees Owing: **$1205**



## 🔎Key Insights
- **103 customers** evaluated baristas
- **16 customers** owe more than **$20 in fees**, contributing to **$1,205 total fees owing**
- **100 total missed orders** across all terms.
- ```PROPER``` and ```LOWER``` functions ensures clean formatting for both names and emails.

---

# 📉4_PIVOT worksheet
## 🔗Link: [Intermediate_Excel_boba](https://github.com/amy941/boba_data_crunch/blob/main/1_Excel_Intermediate_boba/Intermediate_BubbleTea_project.xlsx)

- **Purpose:** Use pivot tables and charts to analyze barista performance by grade and year, identify patterns, and forecast future results.
- **Skills:** `Pivot Tables/Charts/Slicers`, `Percentage of Column Total`, `Data filtering`, `Trendline analysis`, `R-squared`, and `forecasting`
    
## ✨Hightlights
- **First** Pivot Table for Grade Distribution.
- **Second** Pivot Table for Yearly Performance Trend.  
- **Clustered Column Pivot Chart** with Trendlines:
- **Pivot Slicers** were added for **Full Name** of customer, **Barista**, and **Grade**.
- A **Clustered Column Pivot Chart** shows barista performance over time in Linear & Polynomial trendlines.

## 🔎Key Insights

![pivot1](https://github.com/user-attachments/assets/2926e3e3-5be1-45e3-b322-e4e7dc43ef10)

_Screenshot of PivotTables, showing grade distribution by barista as % of column total_

- **A's** (as % of the column total)            
  * Barista Amy: 59.09%                           
  * Barista John: 3.23%
            
-  **C's**:
  * Barista Amy: 0.00%
  * Barista John: 12.90%
    

---

![pivot2](https://github.com/user-attachments/assets/5084e74b-f9bf-4e01-a34b-1df5741e1bca)

_Screenshot of forecast charts, showing performance trends by barista and projected 2025 score using R-squared analysis and trendlines._

- **Polynomial** trendline shows the best fit with **R² = 1**
- If the upward trend continues, **Barista Amy** is forcasted to earn an **average score of 91 in 2025**



---
![slicer](https://github.com/user-attachments/assets/32747ffa-043d-422a-b98e-2e1555a19645)

_Slicers were filtered to show Barista Amy's individual trend._

- The **first eight customers** rated **Amy’s performance** either **A or B**, **no C** given.
- Filtering to **Barista Amy** shows a consistent **upward trend** in performance (from 86 in 2023 to 89 in 2024)
- The **forecasted** score for 2025 is **91**, suggesting continued improvement


---

# 📌CONCLUSIONS
✔️ Barista **Amy’s** performance consistently improved **from 86** (2023) **to 89** (2024), with a **2025 forecast of 91**, showing strong **growth potential**.

✔️ **Polynomial trendline** (R² = 1) indicates strong **predictability** and **reliability** in performance trends.

✔️ Fee collection and missed orders remain rooms for improvement, with **$1,205 outstanding fees** and **100 missed orders** overall.
