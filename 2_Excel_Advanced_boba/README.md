# 📚TABLE OF CONTENTS
- [🧋 Intro](#intro)
- Part 1: VLOOKUP
- Part 2: Macros
---

# 🧋INTRO
This is **Part 2** of the Bubble Tea project where I built a **quote summary and data visualization** for ```Phamily Tea House``` using advanced Excel. 

The focus here is on **Customer Quote** section, covering: 
  * **order management** (location, description, quantity)
  * **pricing calculations** 
  * uncovered key **order patterns**

Together, these perspectives demonstrate how small businesses can use data-driven tools to streamline operations, optimize pricing, and better understand their customers.

## Resources
👉 Click HERE: [Advanced_Excel_boba]()

👉 Click HERE: [raw_data]()

## Sheets Overview
..........................
---

# 📉1_VLOOKUP workbook
## 🔗Link: [Advanced_Excel_boba]()

- **Purpose:** 
- **Skills Applied:**
  * **CHOOSE, VLOOKUP, INDEX-MATCH**
  * **Data formatting** for clear presentation
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

- **Top 3 best-sellers:** `Straw Yog Slush`, `Avocado`, and `Matcha Latte`
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

_Horizontal bar chart summarizing total revenue by location during the first 5 hours of operation._

- **Panorama Hills** sold the most drinks, generating the highest Total Revenue **($739.41)**.
- **Saddle Ridge** ranked second **($510.59)**, followed by **Beltline** ($301.87) and **Brentwood** ($297.06).
- **Country Hills** was the least profitable location **($213.86)**, indicating lower customer activity or smaller orders.
- Spending is **unevenly distributed**, with Panorama Hills and Saddle Ridge together contributing over 60% of total revenue.
- **Panorama Hills is likely a key market** for targeted promotions and resource allocation.

---

![BAR_category](https://github.com/user-attachments/assets/1350fb73-e2c8-43e3-8c31-fb8ebd632298)

_Vertical bar chart showing total revenue by category with trendlines_

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
## 🔗Link: [Advanced_Excel_boba]

- **Purpose:** Create basic macros to automate repetive tasks
- **Skills:** Create, edit, and manage macros efficiently
  
👉 Click HERE: [Advanced_Excel_boba]()

👉 Click HERE: [raw_data]()

- **Create "New Weekly Sales Sheet" Button** for non-macro users to easily navigate
📷📷📷

- **Edit Macro:**
  * Create commamd for Week Commencing Day
📷📷📷

  * Widen the column width: Create a `temp` macro--> Record `temp` macro when auto-widening the column--> Copy & Paste VBA code into the End of original macro
 📷📷📷

- **Relative Reference Macros**
  * Import `SalesDay.csv` files into the system from Legacy Wizards
  * Debug: Comment out the bug
📷📷📷

