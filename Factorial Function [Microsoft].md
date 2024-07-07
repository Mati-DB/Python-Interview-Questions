
# Factorial Function [Microsoft]
Please note that all the information regarding the case study has been sourced from the following [link](https://datalemur.com/questions/python-factorial-formula).

## Index
 - [Interview Question](#Interview-Question)
 - [Solution](#Solution)

***

## Interview Question
Given a number n, write a formula that returns n!.

In case you forgot the factorial formula, **n! = n * (n-1) * (n-2) * ... * 2 * 1**

For example, **5! = 5 * 4 * 3 * 2 * 1 = 120** so we'd return 120

Assume n is a non-negative integer.
***

## Solution

```python
def factorial(n):

  # Initialize x to 1, which will be used to store the result of the factorial calculation
  x = 1

  # Loop through numbers from 1 to n (inclusive)
  for i in range(1,n+1):

    # Multiply x by the current number i and update x
    x = x * i

  # Return the calculated factorial
  return x
```
