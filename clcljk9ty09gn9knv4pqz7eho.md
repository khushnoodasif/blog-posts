# Printing Consonants in a String with Python

Have you ever needed to extract all the consonants from a string in Python? It's a relatively simple task that can be accomplished with just a few lines of code.

First, we start by defining the string we want to work with.

```python
s = "Hello World"
```

Next, we use a `for` loop to iterate through each character in the string. For each character, we use the `isalpha()` method to check if it is an alphabetical character. If it is, we proceed to the next step, which is checking if the character is a consonant.

```python
for char in s:
    if char.isalpha():
```

To check if a character is a consonant, we create a tuple containing all the lowercase vowels and use the `in` operator to check if the lowercase version of the character is in the tuple. If it is not, then we know that the character is a consonant and we print it.

```python
if char.lower() not in ('a','e','i','o','u'):
            print(char)
```

And that's it! With just a few lines of code, we can easily extract all the consonants from a string in Python.

I hope this helps clarify the logic and approach for printing consonants in a string with Python.