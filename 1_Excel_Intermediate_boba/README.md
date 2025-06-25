# Intro
- project: Click [here]
- raw data: Click [here]
- 
# Final Summary worksheet📈
Have a look at the first 3 worksheets, they contain performance scores for each barita from term 1-4. Now go to the Final Summary worksheet and use 3D-Formulas to get performance score average for 3 terms.

## Approach
- **3D-formulas:**
    ```=AVERAGE('Orders Term 1:Orders Term 4'!E4)```
- **Name Ranges:**
  * **Create from Selection** to name each of columns of data

 - **Text Functions:**
  * Use COUNTIFS to calc total number of all performance grades
      
## Storytelling
![final_sum](https://github.com/user-attachments/assets/19ce6450-574a-4757-9113-8bba2a799151)

- Customer Noah Chen graded barista Amy with 91 score (bolded RED)
- Number of B's achieved is 79
- Barista Amy got 13 As, 9 Bs, and none Cs

# Missed Order worksheet📈
Have a look at the worksheets Missed Term 1 through to Term 4, they contain a list of dates that customers didn't pick up their beverage orders. We need to create a summary showing a count of how many days each customer missed their pickup.

## Approach
- Consolidating tool to count days of missed orders for 3 terms

## Storytelling
![missed_order](https://github.com/user-attachments/assets/d050281d-776d-4664-b39b-de31d43d6689)

- 5 distinct customers didn't pick up their drinks for more than 2 orders. They are: CUST0050, 0027, 0052, 0070, and 0079.


# Customer Report worksheet📈
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
![customer_report_1](https://github.com/user-attachments/assets/ac968aa5-5444-4162-8b73-676dba63af89)
![customer_report_2](https://github.com/user-attachments/assets/daa00dbb-f72e-40f6-bac5-6b09a708cf54)

- Total Row shows : 91 as performance score average graded 3 barista from 103 customers, 100 missed orders, $1205 Total Fees Owing.
- filter the table to show 16 customers who owe more than $20


# PIVOT worksheet📈
create a pivot table (in a new sheet) that shows Grade in the Row Labels, Barista in the Column Labels, and Count of Grade in the Values section. How many A's did Barista Amy and John get as a percentage of the column total?
- Barista Amy: 59.09%
- Barista John: 3.23%
How many C's:
- Barista Amy: 0.00%
- Barista John: 12.90%


The owner has observed that the baristas performing their duties seem to be increasingly more able and more motivated. He would like to see if there is a pattern in the results based on year. Create another pivot table to show the average performance final mark by year. Add a filter field and change the filter to only show data for Barista Amy. Format the values to only show 2 decimal places. What was Amy's final performance score in year 2024?
- 88
- 
Create a Clustered Column pivot chart. Add a linear trendline and display the R-squared value on the chart. Question 20
Have a look at the other trend line options and select the one that returns the best R-squared value. Forecast forward for 1 period. If the trend continues, Barista Amy who performs in 2025 are expected to get an average result closest to…
- 91

