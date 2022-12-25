# Writing 1 to 100 in a Text File using Python

In this tutorial, you will learn how to write the numbers 1 to 100 in a text file using Python. Let's get started with the code. If you find this article helpful, please consider sharing it with your coding communities and social media groups so that others can benefit from the content as well.

To write 1 to 100 in a text file, we will follow these steps:

1.  Open the text file in write mode using Python. In this example, we are using a text file called "file.txt" which is located in the same directory as the Python file. We can open the file by simply providing its name, or by specifying the complete file path if it is located elsewhere. Here is the code to open the file in write mode:
    

```python
with open("file.txt","w") as f:
```

2.  Iterate through the range of numbers from 1 to 100 using a for loop. On each iteration, write the current number to the text file using the `write()` function. Don't forget to add a newline character at the end of each line to ensure that each number is on its own line in the text file.
    

```python
for x in range(1,101):
        f.write(str(x) + "\n")
```

Here is the complete code for this program:

```python
with open("file.txt","w") as f:
    for x in range(1,101):
        f.write(str(x) + "\n")
```

Running this code will result in the numbers 1 to 100 being written to the "file.txt" file, with each number on its own line.

I hope this code and explanation are helpful in understanding how to write 1 to 100 in a text file using Python. Thank you for reading!