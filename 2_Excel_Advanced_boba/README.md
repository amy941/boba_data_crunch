# 📚TABLE OF CONTENTS
- [🧋 Intro](#intro)
- Part 1: VLOOKUP
- Part 2: Macros
---

# 🧋🧋INTRO
This is **Part 2** of the Bubble Tea project where I built a **quote summary and data visualization** for ```Phamily Tea House``` using advanced Excel. 

The focus here is on **Customer Quote** section, covering: 
  * **order management** (location, description, quantity)
  * **pricing calculations** 
  * uncovered key **order patterns**

Together, these perspectives demonstrate how small businesses can use data-driven tools to streamline operations, optimize pricing, and better understand their customers.

## Resources
- **Project:** Click [here]()
- **Raw data:** Click [here]()

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



## 📊Data Visualization

![PIE_top_selling](https://github.com/user-attachments/assets/51250adf-ccfd-4c61-9692-2be437b6fc40)

_Pie chart showing % Total Cost by Short Order Description_

- **Top 3 best-sellers:** `Straw Yog Slush`, `Avocado`, and `Matcha Latte`
- **Most popular:** `Straw Yog Slush` 
- **Least popular:** `Chocolate Milk Tea`
- **Fruit-favoured drinks with specialty toppings** drive the highest sales, reflecting a diverse range of customer preferences

---

![COMBO_top_customer](https://github.com/user-attachments/assets/5a772735-d628-44a2-9c79-d38f4218c3b1)

_Clustered Bar & Line showing Top 5 customers with the highest total spending_

- **Lucas Pham** and **Liam Nguyen** were the top spenders
- **Ava Kim**, despite spending less overall, placed the highest number of orders **(12)**, suggesting smaller spending but more frequent purchases.
- Spending (**Total Cost**) vs. Order Quantity (**Qty**) are **not strongly correlate**d. Some customers placed fewer orders but spent more per order.
- The pattern suggests a mix of **high-spend, low-frequency customers** (ex: Lucas Pham) and **frequent, moderate spenders** (ex: Ava Kim)


## 🔎Key Insights
Panorama Hills generated the highest subtotal ($739.41), making it the most profitable order location.

Customers in Category D placed higher-value orders but received the largest discount rates—balancing profit and customer loyalty.

The total order value across all locations is $2,062.78, giving a benchmark for operational and pricing strategies.


Variations in drink prices, quantities, and categories highlight opportunities to optimize pricing and promotions for each region.


---


# 📉2_MACROS workbook
## 🔗Link: [Advanced_Excel_boba]

- **Purpose:** 
- **Skills:**

## ✨Hightlights

      
## 🔎Key Insights



