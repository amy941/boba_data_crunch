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
- [If/Elif]()
- [WHILE/FOR loop]()
- [Data_Visualization]()

👉**Click HERE:** [raw_data]()

---

# 🤔1) If/Elif/Else
## 🔗Link:

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

📷📷📷

✅ **Insights:** After running a few examples, Amy's code successfully provides the **matching categories based on the order cost**. The logic ensures that any **Order Cost is auto-evaluated** and consistently assigned to the **correct Category**, or marked as `No Discount` if it falls outside the discount thresholds.

---

## **Problem 2:** Amy was assigned a new task. This time, her goal is to use the same Sales data to identify customer reward benefits.
- If a customer buys **10 or more drinks**, they get a **Free Drink**.
- If they buy **5 or more drinks**, they grant **5% off on their next drink**.
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

📷📷📷

✅ **Insights:** After testing various scenarios, **Amy’s code correctly applies the reward logic**. Customers are automatically granted the right benefit based on their purchase quantity, ensuring a **fair and consistent reward** distribution.
  
---

# ➿2) While loop and For loop
## 🔗Link:

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

📷📷📷

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
📷📷📷

✅ **Insights:** **Amy's system efficiently categorizes customer feedback**. This allows the team to truly **understand what customers enjoy** and **fine-tune the next specialty** drink for an even better experience.

---

# 📊3) Data Viz:
## 🔗Link:


  



