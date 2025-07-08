# 📚TABLE OF CONTENTS
- [🧋 Intro](#intro)
  - [Resources](#resources)
  - [Sheets Overview](#sheets-overview)
    
- [📉 1_VLOOKUP workbook](#1_vlookup-workbook)
  - [🔢 Excel Formulas Applied](#excel-formulas-applied)
  - [📊 Data Visualization - PIVOT](#data-visualization---pivot)
- [📌 CONCLUSIONS (VLOOKUP)](#conclusions)
  
- [📉 2_MACROS workbook](#2_macros-workbook)
  - [1) Create "New Weekly Sales Sheet" Button](#1-create-new-weekly-sales-sheet-button)
  - [2) Edit Macro](#2-edit-macro)
- [📌 CONCLUSIONS (MACROS)](#conclusions-1)

---

# 🧋INTRO
This is **Part 2** of the Bubble Tea project where I built a **Quote Summary and Data Visualization** for `VieNa Tea House` using advanced Excel. 

The focus here is on **Customer Quote** section, covering: 
  * **Order management** (location, description, quantity)
  * **Pricing calculations** 
  * Uncovered key **order patterns**

Together, these perspectives demonstrate how small businesses can use data-driven tools to streamline operations, optimize pricing, and better understand their customers.

## Resources
👉 Click HERE: [Advanced_Excel_boba]()

👉 Click HERE: [raw_data]()

## Sheets Overview
📊**This data was recorded during the first 5 hours of operations at `VieNa Tea House`**

- **Customer Quote:** Raw data of customer orders.
- **Price List:** Beverage prices and order descriptions for each customer.
- **Discount Matrix:** Discount rates applied based on specific conditions.

---

# 📉1_VLOOKUP workbook
## 🔗Link: [Advanced_Excel_boba]()

- **Purpose:** Pull sales data from other sheets to display a finished and organized Customer Quote.
- **Skills Applied:**
  * **CHOOSE, VLOOKUP, INDEX-MATCH**
  * **Data formatting** for clean presentation
  * Dynamics Lookups with **nested functions** 
  * Data Visualization using **Pivot Tables/Charts**


## 🔢Excel Formulas Applied
- **CHOOSE**: retrieving a value from a list based on a given numeric value. Useful for mapping codes to names.
  
  `=CHOOSE(index_num, value1, [value2], ...)`
  
- **VLOOKUP**: Lookup a matching value of a table, then return a corresponding value from the same row.
  
  `=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])`

- **INDEX-MATCH:** Performs dynamic lookups by row and column. More versatile than VLOOKUP.
  
  `=INDEX(array, row_num, [column_num])` 

  `=MATCH(lookup_value, lookup_array, [match_type])`


![quote_table](https://github.com/user-attachments/assets/295bcbfc-02a7-419b-8ba3-11c6fcf9d446)

| Column                         | Purpose                                                                             | Formula Example                                                                                                            |
| ------------------------------ | ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `D5` - Order Location          | Map location codes to region names                                                  | `=CHOOSE([@[Loc Code]], "Saddle Ridge", "Panorama Hills", "Beltline", "Country Hills", "Brentwood")`                       |
| `F5` - Short Order Description | Retrieve drink description from the Price List sheet                                | `=VLOOKUP([@[Customer ID]], description, MATCH(sales[[#Headers],[Short Order Description]], description[#Headers], 0), 0)` |
| `G5` - Price per Drink         | Retrieve unit price from the Price List sheet                                       | `=VLOOKUP([@[Customer ID]], description, MATCH(sales[[#Headers],[Price per Drink]], description[#Headers], 0), 0)`         |
| `H5` - Order Price             | Calculate total price before discount                                               | `=[@[Qty]] * [@[Price per Drink]]`                                                                                         |
| `I5` - Category                | Assign category based on spending (A → D, lowest → highest) to determine discount % | `=VLOOKUP([@[Order Price]], $M$15:$N$18, 2)`                                                                               |
| `J5` - Discount                | Perform dynamic lookup for discount rate                                            | `=INDEX(Discounts, MATCH([@Category], Discount_Categories, 0), MATCH(J3, Customer_Categories, 0))`                         |
| `K5` - Total Cost              | Calculate final cost after discount                                                 | `=[@[Order Price]] * (1 - [@[Discount]])`                                                                                  |

---


## 📊Data Visualization - PIVOT

![PIE_top_selling](https://github.com/user-attachments/assets/51250adf-ccfd-4c61-9692-2be437b6fc40)

_Pie chart showing % Total Cost by Short Order Description_

- **Top 3 Best-sellers:** `Straw Yog Slush`, `Avocado`, and `Matcha Latte`
- **Most popular:** `Straw Yog Slush` 
- **Least popular:** `Chocolate Milk Tea`
- **Fruit-favoured drinks with specialty toppings** drive the highest sales, reflecting a diverse range of customer preferences

---

![COMBO_top_customer](https://github.com/user-attachments/assets/5a772735-d628-44a2-9c79-d38f4218c3b1)

_Bar & Line Charts showing Top 5 customers with the highest total spending_

- **Lucas Pham** and **Liam Nguyen** were the top spenders
- **Ava Kim**, despite spending less overall, placed the highest number of orders **(12)**, suggesting smaller spending but more frequent purchases.
- Spending (**Total Cost**) vs. Order Quantity (**Qty**) are **not strongly correlated**. Some customers placed fewer orders but spent more per order.
- The pattern suggests a mix of **high-spend, low-frequency customers** (ex: Lucas Pham) and **frequent, moderate spenders** (ex: Ava Kim)

---

![BAR_cost_location](https://github.com/user-attachments/assets/1d05c6a9-6a59-47f2-a1ac-ad68c9d04b3f)

_Horizontal bar chart summarizing Total Revenue by location during the first 5 hours of operation._

- **Panorama Hills** sold the most drinks, generating the highest Total Revenue **($739.41)**.
- **Saddle Ridge** ranked second **($510.59)**, followed by **Beltline** ($301.87) and **Brentwood** ($297.06).
- **Country Hills** was the least profitable location **($213.86)**, indicating lower customer activity or smaller orders.
- Spending is **unevenly distributed**, with Panorama Hills and Saddle Ridge together contributing over 60% of total revenue.
- **Panorama Hills is likely a key market** for targeted promotions and strategic investment.

---

![BAR_category](https://github.com/user-attachments/assets/1350fb73-e2c8-43e3-8c31-fb8ebd632298)

_Vertical bar chart with trendlines showing Total Revenue by Category_

- **Category D** generated the highest total revenue **($1,113.22)**, showing customers spend more in the highest discount category (D).

- Total revenue **increases progressively from Category A to D**, confirming more sales occurred in the highest discount category (D).

- **Polynomial trendline fits best (R² = 0.9998)**, indicating an accelerating growth pattern in spending across discount categories.

---

# 📌CONCLUSIONS

✔️ **Top-sellers**: `Straw Yog Slush`, `Avocado`, and `Matcha Latte` are the best-selling drinks.

✔️ **Customer buying patterns**: `Diverse purchasing habits` - some customers visit less often but spend more per order, while others purchase frequently with smaller totals.
  
✔️ **Location insights**: `Panorama Hills` and `Saddle Ridge` are the key locations driving sales and business growth.

✔️ **Discount impact**: `Top spenders received bigger discounts`, tend to spend more overall, driving the majority of sales.


---


# 📉2_MACROS workbook
## 🔗Link: [Advanced_Excel_boba]()

- **Purpose:** Create basic macros to automate repetitive tasks.
- **Skills:** Create, edit, and manage macros efficiently.
  
👉 Click HERE: [Advanced_Excel_boba]()

👉 Click HERE: [raw_data]()

## 1) **Create "New Weekly Sales Sheet" Button** 
  
![button](https://github.com/user-attachments/assets/d01e42bb-9fdb-4af2-93b6-f4bcd0a00693)

_This button (in Purple) allows non-VBA users to create a brand-new Weekly Sales Sheet automatically_


## 2) **Edit Macro:**
  
✅ **Create a prompt**
    
![commencing_date](https://github.com/user-attachments/assets/c2d0b21f-fc2c-4ac4-8505-1c8e3e8cd271)

_This macro prompts the user to input the `week commencing date` for the new worksheet._

---

✅ **Widen the column width:** Create a `temp` macro--> Record `temp` macro when auto-widening the column(s)--> Copy & Paste the generated VBA code into the End of the main macro

    
![widen_column](https://github.com/user-attachments/assets/bffa4df5-3a6a-4656-9ccd-6d05fd6767fc)

---

✅ **Relative Reference Macros**
  * **Import** Automatically import `SalesDay.txt` files into the system using Legacy Wizards
  * **Debug:** Comment out the bug (in Green)
    
![import_data](https://github.com/user-attachments/assets/2a251c7d-0fd8-48df-b31c-1b98db14dfec)

_This macro used to import sales data from a text file into the worksheet_

---

# 📌CONCLUSIONS

These macros streamline **repetitive Excel tasks** such as `creating new sales sheets`, `adjusting column widths`, and `importing sales data`, making workflows easier for both **VBA and non-VBA users.**
