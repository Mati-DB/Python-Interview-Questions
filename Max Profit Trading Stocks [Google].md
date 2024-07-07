
# Max Profit Trading Stocks [Google]
Please note that all the information regarding the case study has been sourced from the following [link](https://datalemur.com/questions/python-max-profit-trading-stocks).

## Index
 - [Interview Question](#Interview-Question)
 - [Solution](#Solution)

***

## Interview Question
You are given a list of stock ```prices```, where the stock's price on the i<sup>th</sup> day is stored as the 𝑖<sup>th</sup> element of the prices list.

You want to maximize your profit trading the stock, but are only allowed to buy the stock once and sell it once on a future day.

Write a function called ```max_profit``` which takes in this list of stock prices, and computes the max profit possible. Return ```0``` if you can't make any profit.

**Example 1:**

Input: ```prices = [9, 1, 3, 6, 4, 8, 3, 5, 5]``` 
Output: ```7``` 
Explanation: Buy on day 2 (price = 1) and sell on day 6 (price = 8),
𝑝𝑟𝑜𝑓𝑖𝑡 = 8 − 1 = 7

Note that buying on day 2 and selling on day 1 is not allowed because you have to buy the stock BEFORE you can sell it (unless your a time-traveller in which case just trade bitcoin).

**Example 2:**

Input: ```prices = [6, 4, 3, 3, 2]``` 
Output: ```0``` 
Explanation: In this case, no trades should be made since the stock is tanking like a brick. 
The max profit here is ```0```.

***

## Solution

```python
def max_subarray_profit(prices):

    # Create a n empty list to store max subarray profit values (max price in following days - price today )
    subarray_profit = []

    # Loop through each element in prices to find each price and its index
    for i in enumerate(prices):
        index = i[0]
        price = i[1]
        
        # If the index = n-1, break the loop
        if index == len(prices)-1:
            break
        # If the index < n-1:
        else:
            
            # Add the difference between the maximum future value and today's price to the subarray_profit list
            subarray_profit.append(max(prices[index+1:]) - price)
    
    # Calculate the maximum profit possible and return that value        
    max_profit = max(subarray_profit)
    return max_profit 
```
