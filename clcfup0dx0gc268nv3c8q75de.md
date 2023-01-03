# Printing the Last Line of a Text File in Python

Have you ever needed to print out just the last line of a text file in Python? It's a simple task, and can be easily accomplished using a few lines of code.

To start, we'll need to open the text file in read mode using the built-in `open()` function:

```python
with open("demo.txt","r") as f:
```

Next, we'll use the `readlines()` method of the file object to read the contents of the file into a list of strings, with each element representing a line in the file.

```python
line_list = f.readlines()
```

Finally, we can print out the last line of the file by accessing the last element in the list (which is at index `-1`):

```python
print(line_list[-1])
```

And that's it! With just a few lines of code, we've been able to read a text file and print out just the last line. Whether you're a beginner or an experienced programmer, this technique is sure to come in handy at some point in your coding journey.