# Finding the Minimum and Maximum Numbers in a List with Python

Have you ever needed to find the minimum and maximum values in a list in Python? It's a common task, and can be easily accomplished using a simple algorithm.

To start, we'll create a list of numbers and initialize two variables `l_min` and `l_max` with the first element in the list. We'll then iterate through the list, comparing each element to `l_min` and `l_max`. If the current element is less than `l_min`, we'll assign it to `l_min`. If it's greater than `l_max`, we'll assign it to `l_max`.

Here's the complete code for finding the minimum and maximum values in a list:

```python
L = [40,60,12,88,43,22,75,29]

l_max = L[0]
l_min = L[0]

for x in L:
    if x < l_min:
        l_min = x

    if x > l_max:
        l_max = x

print("Minimum Number", l_min)
print("Maximum Number", l_max)
```

And that's it! With just a few lines of code, we've been able to find the minimum and maximum values in a list. Whether you're a beginner or an experienced programmer, this algorithm is sure to come in handy at some point in your coding journey.