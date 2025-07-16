# 📚TABLE OF CONTENTS


---

# 🧋INTRO
This is **Part 3** of the Bubble Tea project where I applied **Python libraries** (NumPy, Pandas, Matplotlib, and Seaborn) to **transform raw CSV data into meaningful insights**. 

The focus here is on:

✅ **Conditional statements:** IF/ELIF/ELSE

✅ **Loops:** WHILE loop & FOR loop

✅ **Data Visualizations:** Graphs (Bar, Scatter Plot, Pie) and descriptive summary

## Resources
👉**Click HERE:**
- [If/Elif](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250708_IF_and_ELIF.ipynb)
- [WHILE/FOR loop](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250709_While_loop_%26_For_loop.ipynb)
- [Data_Visualization](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)

👉**Click HERE:** [raw_data](https://github.com/amy941/boba_data_crunch/tree/main/raw_data/Python_raw)

---

# 🤔1) If/Elif/Else
## 🔗Link: [If/Elif](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250708_IF_and_ELIF.ipynb)

## **Problem 1:** Amy is a data professional for `VieNa Tea House`. Her task is to leverage Sales Summary data to categorize discounts based on order cost ranges.

✅ **Solution:** Using `def` function & conditional statments `IF/ELIF` to automate this process.

```
def discount_category (order_cost):
    if order_cost == 6.25:
        print('Category A')
    elif 15.50 <= order_cost <= 20.50:
        print('Category B')
    elif 20.50 <= order_cost <= 30.5:
        print('Category C')
    elif order_cost >= 30.50:
        print('Category D')
    else:
        print('No Discount')

# Example:
discount_category(60.50)
discount_category(5.50)
discount_category(25.75)
discount_category(19.75)
```

![if](https://github.com/user-attachments/assets/cc85f189-7d10-4146-a4c0-217a52d5b664)

✅ **Insights:** After running a few examples, Amy's code successfully provides the **matching categories based on the order cost**. The logic ensures that any **Order Cost is auto-evaluated** and consistently assigned to the **correct Category**, or marked as `No Discount` if it falls outside the discount thresholds.

---

## **Problem 2:** Amy was assigned a new task. This time, her goal is to use the same Sales data to identify customer reward benefits.
- If a customer buys **10 or more drinks**, they get a **Free Drink**.
- If they buy **5 or more drinks**, they receive **5% off on their next drink**.
- Otherwise, **no reward.**


✅ **Solution:** Using `def` function & conditional statements `IF/ELIF` to automate the reward logic.

```
def reward_customer(num_drinks, discount_threshold, free_drink_threshold):
    if num_drinks >= free_drink_threshold:
        print('🎉Congrats! You earn 1 free drink.')
    elif num_drinks >= discount_threshold:
        print('👏Congrats! 5% off on your next drink.')
    else:
        print('🍵 Keep sipping! Good luck next time!')

# Example:
reward_customer(12, discount_threshold=5, free_drink_threshold=10)  # 1 free
reward_customer(6, discount_threshold=5, free_drink_threshold=10)   # 5% off
reward_customer(3, discount_threshold=5, free_drink_threshold=10)   # None
```

![if_1](https://github.com/user-attachments/assets/02515586-63c2-48f1-9290-b3b6f13e9182)

✅ **Insights:** After testing various scenarios, **Amy’s code correctly applies the reward logic**. Customers are automatically granted the right benefit based on their purchase quantity, ensuring a **fair and consistent reward** distribution.
  
---

# ➿2) While loop and For loop
## 🔗Link: [WHILE/FOR loop](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250709_While_loop_%26_For_loop.ipynb)

## **Problem 1:** `VieNa Tea House` offers a `Buy 2 Get 1 Free` deal on the first Tuesday of each month through their website. Customers have limited time to complete their orders. 
Amy was asked to create a system that starts a **10-minute countdown**. During the countdown:
   * At **5 minutes**, print: "⏰ Clock is ticking. Finishing up your order! 5 minutes remaining."
   * At **2 minutes**, print: "⚠️ Don't lose the reward! 2 minutes remaining."
   * At **0 minutes**, print: "❌ User timed out. Please try again!"

✅ **Solution:** Using a `while` loop, `if/elif` statements, and `sleep()` function to simulate a real-time countdown.

```
from time import sleep

mins = 10

while mins >= 0:
    if mins == 5:
        print('⏰ Clock is ticking. Finishing up your order! 5 minutes remaining.')
    elif mins == 2:
        print('⚠️ Don\'t lose the reward! 2 minutes remaining.')
    elif mins == 0:
        print('❌ User timed out. Please try again!')
    else:
        print(mins)

    mins -=1
    sleep(1)
```

![while](https://github.com/user-attachments/assets/039b681c-2947-4137-afaf-eadc4d8c9b05)

✅ **Insights:** **Amy’s countdown timer works** as intended, providing **timely reminders** and prompting users to **complete their orders** before the offer expires. The logic creates a simple yet effective user experience that encourages faster checkout.

---

## **Problem 2:** `VieNa Tea House` collected customer ratings (1–10) for their monthly specialty `Crème Brûlée Milk Tea`, where 10 is the best. 
They want to classify the feedback into three categories:
   * **Negative** (scores of 1-5)
   * **Neutral** (scores of 6-8)
   * **Positive** (scores of 9-10)

Amy was then asked to build a system that processes a list of integer scores and counts how many fall into each category.

     
✅ **Solution:** Using a `for` loop, `if/elif` statements to iterate through the list, classify each score, and count the totals.

```
def customer_feedback(score_list):
    negative_scores = 0
    neutral_scores = 0
    positive_scores = 0

    for score in score_list:
        if score >= 9:
            positive_scores += 1
        elif score >= 6:
            neutral_scores += 1
        else:
            negative_scores += 1

    print('😋 Yummy:', positive_scores)
    print('😐 So-so:', neutral_scores)
    print('🤢 Bad:', negative_scores)
```

✅ **Insights:** Amy's system **efficiently categorizes customer feedback**. This allows the team to truly **understand what customers enjoy** and **fine-tune the next specialty** drink for an even better experience.

---

# 📊3) Data Viz:
## 🔗Link: [Data_Visualization](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)

## 📝 1) Descriptive Summary: Amy was asked to conduct `exploratory data analysis (EDA)` on the Sales data.
- She used **methods** and **attributes** such as `head()`, `.shape`, `.dtypes`, `.drop_duplicates()` to study and clean the CSV raw data.
- She then applied `sort_values()` by **Qty** to find out the customer with the most orders.
- Lastly, she sorted the data by **Price per Drink** to identify the most expensive drink.

```
# Most expensive drink(s)
boba.sort_values(by='Price per Drink', ascending=False).head()
```

![expensive_drink](https://github.com/user-attachments/assets/6bd6e1c2-910c-491b-9c26-faac34e8694b)

✅ **Key Findings:**

✔️ Dataset has **100 rows** and **11 columns**, with **0 duplicates**

✔️ Data types include **5 objects**, **2 integers**, and **4 floats**.

✔️ **Ethan Tran** ranked first with **7 orders**, followed by Olivia Hoang and Ethan Kim.

✔️ `Brown Sugar MT` and `Avocado Slush` are the **most costly drinks**
  

👉👉👉For more information: Click [HERE](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)

---

## 📊 2) Data Visualization: Amy was then asked to plot different data viz to gain visual understanding and insights.

### 📉 Box plot: to show how Sales vary across locations.

```
# Boxplot 1: Order Location vs. Total Cost
boxplot1 = sns.boxplot(data=boba,
                      x='Order Location',
                      y= 'Total Cost')
boxplot1.set_title('Order Location vs. Total Cost')  # shows how Total Cost varies across locations.

plt.show(boxplot1)
```
![box_plot](https://github.com/user-attachments/assets/876bd3ac-b0d4-43b3-90db-0952a8f88c9e)

✔️ **Beltline** & **Country Hills** have the **highest median** Total Cost (>30), meaning customers tend to **place bigger orders** in these locations.

✔️ **Saddle Ridge** & **Panorama Hills** show a **average median** (~20), suggesting **moderate spending** per order.

✔️ **Brentwood** has the **lowest median** (~12), showing **customers spend less** per order in this area.


👉👉👉For more information: Click [HERE](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)

---

### 📉 Bar charts: to determine the most profitable location and Top 5 Best-selling drinks

```
# Bar plot: Order Location vs. Total Cost

# Group by 'Order Location' and sum of 'Total Cost'
sales_by_location = boba.groupby('Order Location')['Total Cost'].sum().reset_index()

# Plot
plt.figure(figsize=(8,6))
sns.barplot(data=sales_by_location,
           x= 'Order Location',
           y= 'Total Cost')

plt.xlabel('Location')
plt.ylabel('Total Sales ($)')
plt.title('Total Sales ($) by Order Location')
plt.xticks(rotation=45)

plt.show()
```

![location](https://github.com/user-attachments/assets/1fcf6873-b174-42ae-9966-1dbf884fe662)

✔️ **Panorama Hills** generates the **highest Revenue** (>700$), followed by **Saddle Ridge** (~500$)

✔️ **Beltline** & **Brentwood** earn **similar sales** (~300$).

✔️ **Country Hills** records the **lowest revenue** (~200$). 

✔️ `Oolong MT` is the **best-selling beverage** while `Passion Fruit Tea` is the **least popular** one.


👉👉👉For more information: Click [HERE](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)

---

### 📉 Scatter plot: `Qty` vs. `Total Cost`

```
plt.figure(figsize=(8,6))
plt.scatter(boba['Qty'], boba['Total Cost'])

plt.xlabel('Quantity')
plt.ylabel('Total Cost ($)')
plt.title('Quantity vs. Total Cost ($)')

plt.show()
```

![scatter](https://github.com/user-attachments/assets/9a70c15b-915b-469a-a544-2f4fc03ef393)

✔️ Relationship between **Total Cost** and **Quantity** is almost **linear**, meaning each drink contributes evenly to the total bill.

✔️ **Cost variation** due to differences in prices.

✔️ **No major Outliers**, showing **consistent patterns** across most orders.


👉👉👉For more information: Click [HERE](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)

---

### 📉 Pie chart: Total Sales by Order Location

```
# PIE Chart: Category vs. Total Cost
discount_by_category = boba.groupby('Category')['Total Cost'].sum()

# Create the pie chart
plt.figure(figsize=(4, 4))
plt.pie(
    discount_by_category,
    labels= discount_by_category.index,
    autopct= '%1.1f%%',
    startangle= 90
)

plt.title('Discount % by Category')
plt.show()
```
![pie_chart](https://github.com/user-attachments/assets/635e55cd-df91-428f-a588-d96cfc0aefcd)

✔️ **Cat. D** holds the majority share (54.0%), meaning it **contributes over half** of all discounts, followed by **Cat. C** (21.6%)

✔️ **Cat. A** and **B** contribute the smallest shares (16.1% and 8.4%, respectively)


👉👉👉For more information: Click [HERE](https://github.com/amy941/boba_data_crunch/blob/main/3_Python/20250710_Data_Visualizations_with_Python.ipynb)


# 📌 CONCLUSIONS
.....................................................................
