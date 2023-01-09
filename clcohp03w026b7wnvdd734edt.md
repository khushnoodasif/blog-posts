# Finding the Frequency of a Word in a Text File with Python

Have you ever needed to find out how many times a particular word appears in a text file using Python? It's a common task that can be easily accomplished with just a few lines of code.

First, we start by asking the user to enter the word whose frequency they want to find. We store this word in a variable `k` and initialize a counter variable `count` to 0.

```python
Copy codek = input("Enter the word")
count = 0
```

Next, we open the text file in read mode and use the `read()` method to read the entire contents of the file into a string variable `data`.

```python
with open("content.txt","r") as f:
    data = f.read()
```

Then, we use the `split()` method to split the string into a list of words, and use a `for` loop to iterate through each word. For each word, we use an `if` statement to check if it is equal to the word the user is interested in. If it is, we increment the `count` variable by 1.

```python
for word in data.split():
    if word == k:
        count += 1
```

Finally, we print the value of `count` to display the frequency of the word in the text file.

```python
print(count)
```

And that's it! With just a few lines of code, we can easily find the frequency of a word in a text file using Python.

I hope this helps clarify the logic and approach for finding the frequency of a word in a text file with Python