# Displaying Lines from a Text File in Python

Have you ever needed to display the contents of a text file in Python? It's a common task, and can be easily accomplished using a few simple lines of code.

To start, we'll need to open the text file in read mode. We can do this using the built-in `open()` function, like so:

```python
with open("content.txt","r") as f:
```

Next, we'll need to read the contents of the file into a string. We can do this using the `read()` method of the file object:

```python
data = f.read()
```

Now that we have the contents of the file stored in a string, we can split the string at the newline character (`\n`) to get a list of individual lines. We can then iterate through this list and print out each line:

```python
for line in data.split("\n"):
    print(line)
```

And that's it! With just a few lines of code, we've been able to read a text file and display its contents line by line. Whether you're a beginner or an experienced programmer, this technique is sure to come in handy at some point in your coding journey.