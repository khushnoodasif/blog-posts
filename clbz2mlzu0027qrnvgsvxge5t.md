# Filtering Lines from a Text File Based on Length using Python

In this tutorial, we will learn how to read lines from a text file and display only those lines that have a length greater than 50 using Python. Here is the logic and explanation of the program:

1.  First, we need to open the text file in read mode in our Python program. To do this, we use the following command:
    

```python
f = open("content.txt","r")
```

Here, the name of the text file is "content.txt" and it is present in the same directory as this Python file. If the text file is located elsewhere, you will need to specify the complete path to the file.

2.  Next, we iterate through the content of the file, where each iteration corresponds to a line in the file. For each line, we check its length using the `len()` function.
    

```python
for line in f:
    l = len(line)
```

3.  If the length of the line is greater than 50, we print the line to the console using the `print()` function.
    

```python
if l > 50:
    print(line)
```

Here is the complete source code for the program:

```python
f = open("content.txt","r")
for line in f:
    l = len(line)
    if l > 50:
        print(line)
```

I hope this helps! Let me know if you have any questions or need further assistance.