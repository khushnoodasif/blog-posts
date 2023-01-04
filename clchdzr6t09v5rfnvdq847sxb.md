# Printing Odd Numbers Between Two Numbers in Python

Have you ever needed to print out a range of odd numbers in Python? It's a simple task, and can be easily accomplished using a few lines of code.

To start, we'll need to get the starting and ending numbers from the user. We can do this using the built-in `input()` function:

```python
n1 = int(input("Enter starting no"))
n2 = int(input("Enter ending no"))
```

Next, we'll use a `for` loop to iterate through all the numbers between `n1` and `n2`. Inside the loop, we'll check each number to see if it's odd by checking the remainder of the number when it's divided by 2. If the remainder is non-zero, we know the number is odd and can print it out:

```python
for x in range(n1+1,n2):
    if x%2 != 0:
        print(x)
```

And that's it! With just a few lines of code, we've been able to print out a range of odd numbers. Whether you're a beginner or an experienced programmer, this technique is sure to come in handy at some point in your coding journey.