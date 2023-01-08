# Splitting a String at the First Occurrence of a Character in Python

Have you ever needed to split a string at the first occurrence of a particular character in Python? It's a common task that can be easily accomplished using the `find()` method and string slicing.

First, let's define the string we want to work with and the character at which we want to split it.

```python
s = "Python Programming" 
k = input("Enter character at which you want to split") 
```

Next, we use the `find()` method to locate the index of the first occurrence of the character `k` in the string.

```python
i = s.find(k)  
```

Finally, we use string slicing to split the string into two parts. The first part is from the start of the string (index 0) to one index less than the index of the character `k`. The second part is from the index of the character `k` plus one to the end of the string.

```python
print('First Part: ', s[:i]) 
print('Second Part: ', s[i+1:])
```

And that's it! With just a few lines of code, we can easily split a string at the first occurrence of a character in Python.

I hope this helps clarify the logic and approach for splitting a string at the first occurrence of a character in Python.