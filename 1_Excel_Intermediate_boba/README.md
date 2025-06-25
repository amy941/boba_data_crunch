# Intro
- project: Click [here]
- raw data: Click [here]

---

# 1_FINAL SUMMARY worksheet📉
- **Purpose:** Final Summary worksheet dives into customer feedback to evaluate barista performance across four terms.
- **Skills:** 3D-Formulas, Linking worksheets, Named Ranges, and Text functions.
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

![final_sum](https://github.com/user-attachments/assets/7bce0768-ec6d-42b9-ac8c-b43e5859fb5f)

---

# 2_MISSED ORDER worksheet📈
- **Purpose:** Track and summarize customer no-shows across Terms 1–4 by counting missed drink pickups.
- **Skills:** Consolidation, Sort & Filter, Conditional Formatting
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
Go to the Customer Report worksheet. Some of the information still needs to be completed. Create a formula in E4 to return the Customer's full name, this should be First Name followed by a space and then Surname. The case must also be corrected so that all words start with a capital letter but everything else is in lower case e.g., Ava Hoang
Question 9
In F4 create a formula to generate the customer email address. This should be their first initial, followed by their surname, followed by "@bbt.com", and must all be in lower case, e.g. ahoang@bbt.com. 
In G4 create a formula that will put "2015-" followed by the last three digits of the Customer ID, e.g. 2015-001.
We would like to get an idea of how baristas have progressed over the year. Create a sparkline line chart that charts the data. Change the sparkline to show the highest point. Which of these sparklines represents Liam Kims' data?

# Approach
Use nest functions with text functions (ex: PROPER, LOWER, UPPER, ...)
- Full name: =PROPER(CONCAT(B4," ",C4))
- Email: =LOWER(CONCAT(LEFT(B4,1),C4,"@bbt.com"))
- ID: =CONCAT(2015,"-",RIGHT(A4,3))
![customer_report_1](https://github.com/user-attachments/assets/61d457ab-7002-45f0-9e9e-bcce155ffee3)

![customer_report_2](https://github.com/user-attachments/assets/1b879f17-172b-40b5-bad0-f3c056c8165f)

- Total Row shows : 91 as performance score average graded 3 barista from 103 customers, 100 missed orders, $1205 Total Fees Owing.
- filter the table to show 16 customers who owe more than $20
![total_row](https://github.com/user-attachments/assets/32d8e656-85bf-4776-8a08-22a89d8028e4)

![sparkline](https://github.com/user-attachments/assets/51da85e0-797b-4a5e-a58a-a5d0b3d55bb6)

---

# PIVOT worksheet📉
create a pivot table (in a new sheet) that shows Grade in the Row Labels, Barista in the Column Labels, and Count of Grade in the Values section. How many A's did Barista Amy and John get as a percentage of the column total?
- Barista Amy: 59.09%
- Barista John: 3.23%
How many C's:
- Barista Amy: 0.00%
- Barista John: 12.90%

![pivot1](https://github.com/user-attachments/assets/2926e3e3-5be1-45e3-b322-e4e7dc43ef10)

The owner has observed that the baristas performing their duties seem to be increasingly more able and more motivated. He would like to see if there is a pattern in the results based on year. Create another pivot table to show the average performance final mark by year. Add a filter field and change the filter to only show data for Barista Amy. Format the values to only show 2 decimal places. What was Amy's final performance score in year 2024?
- 88
- 
Create a Clustered Column pivot chart. Add a linear trendline and display the R-squared value on the chart. Question 20
Have a look at the other trend line options and select the one that returns the best R-squared value. Forecast forward for 1 period. If the trend continues, Barista Amy who performs in 2025 are expected to get an average result closest to…
- 91

![pivot2](https://github.com/user-attachments/assets/5084e74b-f9bf-4e01-a34b-1df5741e1bca)
