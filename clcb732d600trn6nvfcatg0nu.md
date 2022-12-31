# Using List Comprehension to Get a List of Square Roots of Odd Numbers in Python

List comprehension is a concise way to create a list using a single line of code. It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. The result is a new list that is the result of evaluating the expression in the context of the for and if clauses.

In this tutorial, we'll be using list comprehension to create a list of the square root of all odd numbers between 1 and 20. Here's the code for that:

```python
odd_numbers = [i for i in range(1,21) if i % 2 != 0]
square_roots = [number ** 0.5 for number in odd_numbers]
print(square_roots)
```

This code creates a list called `odd_numbers` that contains all of the odd numbers between 1 and 20. It then creates a new list called `square_roots` using list comprehension, where the square root of each number in `odd_numbers` is calculated and added to the list. Finally, the list of square roots is printed to the console.

Alternatively, you can use the `math` module in Python to find the square root of a number. Here's the code for that:

```python
import math
odd_numbers = [i for i in range(1,21) if i % 2 != 0]
square_roots = [math.sqrt(number) for number in odd_numbers]
print(square_roots)
```

This code works in the same way as the previous example, but instead of using the exponentiation operator (`**`) to calculate the square root, it uses the `sqrt()` function from the `math` module.

And that's it! With just a few lines of code, you can use list comprehension to create a list of the square root of all odd numbers between 1 and 20 in Python.