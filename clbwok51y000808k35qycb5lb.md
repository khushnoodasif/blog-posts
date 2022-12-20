# Searching a string in a list of strings using a loop in Python

In this tutorial, we will learn how to search a string in a list of strings using a loop in Python. We will start by explaining the logic behind the program, then we will provide the source code and finally, we will see some examples of its output.

# Logic

To search a string in a list of strings, we will iterate through all the elements of the list one by one and check whether any of the elements match the string we are looking for. To do this, we will use a for loop and an if statement.

First, we will define a list of strings, for example:

```python
words = ["apple", "banana", "cherry", "date", "elderberry", "fig", "grape"]
```

Then, we will ask the user to input the string to be searched in the list.

```python

word_to_search = input("Enter a word to search: ")
```

To keep track of whether the element has been found or not, we will create a variable called `found` and initialize it to `False`.

```python
found = False
```

Now, we will use a for loop to iterate through all the elements of the list. At every run of the loop, the `word` variable will have the value of the current element of the list.

```python
for word in words:
```

Inside the loop, we will use an if statement to check whether the element matches the string entered by the user. If it does, we will set the `found` variable to `True`.

```python
if word == word_to_search:
        found = True
```

Finally, we will give a final message according to the value of the `found` variable. If it is `True`, we will print that the element is present in the list. Otherwise, we will print that the element is not present in the list.

```python
if found == True:
    print(esearch, "is present in list")
else:
    print(esearch, "is not present in list")
```

# Source Code

Here is the complete source code of the program:

```python
word_to_search = input("Enter a word to search: ")
found = False

for word in words:
    if word == word_to_search:
        found = True

if found:
    print(word_to_search, "is present in the list.")
else:
    print(word_to_search, "is not present in the list.")
```

This code will ask the user to enter a word to search, then it will loop through the list of words and check if any of them match the word entered by the user. If a match is found, the code will print that the word is present in the list. If no match is found, the code will print that the word is not present in the list.

# Output

Here are some examples of the output of the program:

```python

Enter element to be searched Like
Like is present in list
```

```python
Enter element to be searched Bye
Bye is not present in list
```

I hope this helps! Let me know if you have any questions.