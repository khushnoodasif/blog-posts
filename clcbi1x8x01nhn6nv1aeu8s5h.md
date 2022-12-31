# Counting the Number of Long Words in a Text File with Python

In this tutorial, we will learn how to write a Python program to read a text file and count the number of words whose length is greater than 5.

To begin, we will start by opening the text file in read mode and storing its contents in a string. We can do this using the `with open` function in Python.

```python
with open("content.txt", "r") as f:
    data = f.read()
```

Next, we will iterate through the data string, word by word, and use a conditional statement to check the length of each word. If the length of a word is greater than 5, we will increment a count variable by 1.

```python
count = 0
for word in data.split():
    if len(word) > 5:
        count += 1
```

Finally, we can print the result by printing the count variable.

```python
print("No of Word whose length greater than 5", count)
```

It's worth noting that we are using the `split()` function to split the data string into a list of words. This function splits the string at each space by default.

Additionally, when using the `with open` function to open a file in Python, we don't need to close the file separately as it will be closed automatically.

I hope this tutorial was helpful and you were able to understand how to write a Python program to read a text file and count the number of words whose length is greater than 5. If you have any questions or doubts, feel free to leave a comment below.