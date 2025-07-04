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
  
  `=CHOOSE(**index_num**, value1, [value2], ...)`
  
- **VLOOKUP**: Lookup a matching value of a table, then return a corresponding value from the same row.
  
  `=VLOOKUP(**lookup_value**, table_array, col_index_num, [range_lookup])`

- **INDEX-MATCH:** Performs dynamic lookups by row and column. More versatile than VLOOKUP.
  
  `=INDEX(**array**, row_num, [column_num])
  and =MATCH(**lookup_value**, lookup_array, [match_type])`

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

## 🔎Key Insights

---

# 📉2_MACROS workbook
## 🔗Link: [Advanced_Excel_boba]

- **Purpose:** 
- **Skills:**

## ✨Hightlights

      
## 🔎Key Insights



