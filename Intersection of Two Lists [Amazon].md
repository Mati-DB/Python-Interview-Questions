
# Intersection of Two Lists [Amazon]
Please note that all the information regarding the case study has been sourced from the following [link](https://datalemur.com/questions/python-intersection-of-two-lists).

## Index
 - [Interview Question](#Interview-Question)
 - [Solution](#Solution)

***

## Interview Question
Write a function to get the intersection of two lists.

For example, if A = [1, 2, 3, 4, 5], and B = [0, 1, 3, 7] then you should return [1, 3].
***

## Solution

```python
def intersection(a, b):
    # Create an empty list to store the common elements
    intersect = []

    # Loop through each element in the first list (a)
    for i in a:
        
        # Check if the current element is also in the second list (b)
        if i in b:
            
            # If true, add the element to the intersect list
            intersect.append(i)
            
        else:
            
            # If false, skip to the next iteration
            continue
    
    # Return the list of common elements
    return intersect
```
