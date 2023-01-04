# Printing Factors of a Number in Python

Have you ever needed to find and print the factors of a number in Python? It's a simple task, and can be easily accomplished using a few lines of code.

To start, we'll need to get the number from the user using the built-in `input()` function:

```python
n = int(input("Enter a Number"))
```

Next, we'll use a `for` loop to iterate through all the numbers from 1 to `n`. Inside the loop, we'll check to see if the current number is a factor of `n` by checking the remainder of `n` when it's divided by the current number. If the remainder is zero, we know the current number is a factor and can print it out:

```python
for x in range(1,n+1):
    if n%x == 0:
        print(x)
```

And that's it! With just a few lines of code, we've been able to find and print the factors of a number. Whether you're a beginner or an experienced programmer, this technique is sure to come in handy at some point in your coding journey.