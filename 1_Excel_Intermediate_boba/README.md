# INTRO
- project: Click [here]
- raw data: Click [here]

---

# 1_FINAL SUMMARY worksheet📉
- **Purpose:** Final Summary worksheet dives into customer feedback to evaluate barista performance across four terms.
- **Skills:**
  * 3D-Formulas
  * Linking worksheets
  * Named Ranges
  * Text functions
- **Outcome:** Aggregated performance scores, sugar/ice preferences, and overall grading insights.

## Hightlights✨
- **3D-formulas:** to calc. average scores across Term 1-4
    ```=AVERAGE('Orders Term 1:Orders Term 4'!E4)```
- **Name Ranges:** ```Create from Selection``` for clean, readable format.
- **COUNTIFS and Conditional Formatting** to track & highlight grade distribution.
      
## Key Insights🔎
- Customer **Noah Chen** gave **Barista Amy** a top score of **91** (highlighted in RED)
- **Barista Amy** earned: 13 A's, 9 B's, and 0 C's
- **Total B grades:** **79** across all baristas
- The average customer prefers **moderate sugar (40-60%)** and **light to moderate ice (25-50%)**

![final_sum](https://github.com/user-attachments/assets/241a05cd-f704-430d-ba27-0b16d2c5a0d0)

---

# 2_MISSED ORDER worksheet📈
- **Purpose:** Track and summarize customer no-shows across Terms 1–4 by counting missed drink pickups.
- **Skills:**
  * Consolidation
  * Sort & Filter
  * Conditional Formatting
- **Outcome:** A ranked summary of customers who missed pickups, including frequent no-shows flagged in red.

## Hightlights✨
- **Consolidation Tool** used to merge data from ```Missed Term 1``` to ```Missed Term 4```
- **Sorting** missed pickup from smallest to largest
- **Conditional Formatting** to highlight customers who missed **2 or more orders.**
      
## Key Insights🔎
- Most customers missed only **one pickup**
- **5 customers** missed **2 or more** drink pickups: ```CUST0050```, ```CUST0027```, ```CUST0052```, ```CUST0070```, ```CUST0079```
- **CUST0079** is the highest no-show with **3 missed orders**
  
![missed_order](https://github.com/user-attachments/assets/7ee48e35-5d81-4ed0-831c-6b10d5065127)


---

# CUSTOMER REPORT worksheet📉
- **Purpose:** Transform raw customer data into a clean format and analyze individual performance trends across four terms.
- **Skills:**
  * Text functions (```CONCAT```, ```PROPER```,```UPPER```, ```LEFT```, ```RIGHT```, etc.)
  * Nested formulas (```LOWER(CONCAT(LEFT(...)))```)
  * Conditional functions (```SUMIFS```, ```COUNTIFS```,etc.)
  * Sparkline charts
  * Sort & Filter
- **Outcome:** A clean and consistent customer report featuring:
  * Full Names, Emails, ID tags
  * Performance trends
  * Summary of fees & missed orders. 

## Hightlights✨
- **Text Functions** to format data:
  * Full Name (e.g., Ava Hoang)
    
    ```=PROPER(CONCAT(B4," ",C4))```
    
  * **Email Address** (e.g., ahoang@bbt.com)
    
    ```=LOWER(CONCAT(LEFT(B4,1),C4,"@bbt.com"))```
    
  * **ID tags** (e.g., 2015-001)

    ```=CONCAT(2015,"-",RIGHT(A4,3))```

![customer_report_1](https://github.com/user-attachments/assets/61d457ab-7002-45f0-9e9e-bcce155ffee3)


- **Sparklines** to visualize how baristas have progressed over the year.
  * Use **High Point** markers to highlight performance peaks.
  * Example: Barista Tom's peak performance score is 86 in Term 3, graded by Liam Kim, visible in the orange dot.

![sparkline](https://github.com/user-attachments/assets/51da85e0-797b-4a5e-a58a-a5d0b3d55bb6)

- **Structured Table** with ```Total Row``` enabled:
  * Average Performance Final Score: **91**
  * Total Missed Orders: **100**
  * Total Fees Owing: **$1205**

![total_row](https://github.com/user-attachments/assets/32d8e656-85bf-4776-8a08-22a89d8028e4)


## Key Insights🔎
- **103 customers** evaluated the performance of 3 baristas across four terms.
- **16 customers** owe more than **$20 in fees**, contributing to **$1,205 total fees owing**
- **100 total missed orders** across all terms.
- ```PROPER``` and ```LOWER``` functions ensures clean formatting for both names and emails.

---

# PIVOT worksheet📉
- **Purpose:** Use pivot tables and charts to analyze barista performance by grade and year, identify patterns, and forecast future results.
- **Skills:**
  * Pivot Tables & Pivot Charts
  * Percentage of column total
  * Data filtering
  * Trendline analysis, R-squared interpretation, and forecasting
- **Outcome:**
  * Grade distribution by barista
  * Year-over-year performance trend
  * Forecast for future performance using the best-fitting trendline
## Hightlights✨
- First **Pivot Table** for Grade Distribution:
  * **Row Labels:** Grade (A, B, C)
  * **Column Labels:** Barista
  * **Values:** Count of Grade (shown as % of column total)

- Second **Pivot Table** for Yearly Performance Trend:
  * Shows **average final performance scores by year**
  * Filter applied to display only **Barista Amy**
  * Values formatted to **2 decimal places**

- **Clustered Column Pivot Chart** with Trendlines:
  * **Linear** and **Polynomial** trendlines
  * **R-squared** values to assess model fit
    
## Key Insights🔎
- **A's** (as % of the column total?)
  * Barista Amy: 59.09%
  * Barista John: 3.23%
  
-  **C's**:
  * Barista Amy: 0.00%
  * Barista John: 12.90%
    
![pivot1](https://github.com/user-attachments/assets/2926e3e3-5be1-45e3-b322-e4e7dc43ef10)

- **Polynomial** trendline shows the best fit with **R² = 1**
- If the upward trend continues, **Barista Amy** is forcasted to earn an **average score of 91 in 2025**

![pivot2](https://github.com/user-attachments/assets/5084e74b-f9bf-4e01-a34b-1df5741e1bca)

---

# CLOSING THOUGHTS
_This part of the Boba Project transforms real-world business scenarios into powerful insights. By applying intermediate Excel skills, the data is presented in a clean, consistent, and more engaging format. Most importantly, it reveals patterns that can drive strategic decisions. And that’s the heart of analytics — not just crunching numbers, but telling honest stories with data._

