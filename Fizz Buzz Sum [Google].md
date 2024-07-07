
# Fizz Buzz Sum [Google]
Please note that all the information regarding the case study has been sourced from the following [link](https://datalemur.com/questions/python-fizz-buzz-sum).

## Index
 - [Interview Question](#Interview-Question)
 - [Solution](#Solution)

***

## Interview Question
Write a function fizz_buzz_sum to find the sum of all multiples of 3 or 5 below a target value.

For example, if the target value was 10, the multiples of 3 or 5 below 8 are 3, 5, 6, and 9.

Because **3 + 5 + 6 + 9 = 23** our function would return 23.
***

## Solution

```python
def fizz_buzz_sum(target):
    # Create an empty list to store the numbers
    addends = []
  
    # Loop through numbers from 1 to target-1
    for i in range(1, target):
        
        # Check if the current number is divisible by 3 or 5
        if i % 3 == 0 or i % 5 == 0:
            
            # If true, add the number to the addends list
            addends.append(i)

        else:
            
            # If false, skip to the next iteration
            continue
    
    # Calculate the sum of all numbers in the addends list
    addition = sum(addends)
    
    # Return the calculated sum
    return addition
```
