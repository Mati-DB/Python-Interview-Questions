
# Contains Duplicate [Apple]
Please note that all the information regarding the case study has been sourced from the following [link](https://datalemur.com/questions/python-contains-duplicate).

## Index
 - [Interview Question](#Interview-Question)
 - [Solution](#Solution)

***

## Interview Question
Given an list of integers called ```input```, return ```True``` if any value appears at least twice in the array. Return False if every element in the input list is distinct.

For example, if the input list was ```[1,3,5,7,1]```, then return ```True``` because the number 1 shows up twice.

However, if the input was ```[1,3,5,7]``` then return ```False```, because every element of the list is distinct.
***

## Solution

```python
def contains_duplicate(input):

    # Compare the length of the input list against the same list transformed to a set as they don't admit duplicate elements
    if len(input) != len(set(input)):

        # If their length is different, then there are duplicate numbers 
        return True

    else:

        # If their length is the same, then there are no duplicates
        return False
```
