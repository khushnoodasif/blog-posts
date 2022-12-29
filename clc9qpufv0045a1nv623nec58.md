# Python Program to Find and Remove Duplicate Lines in a Large Text File

To find and remove duplicate lines in a large text file, we can follow these steps:

1.  Open the text file in read mode:
    

```python
with open("content.txt", "r") as f:
```

2.  Read the lines of the file and store them in a list:
    

```python
linelist = f.readlines()
```

3.  Create a temporary list to store the unique lines:
    

```python
R = []
```

4.  Iterate through the lines in the `linelist` and check if they are present in the temporary list. If they are not present, append them to the temporary list:
    

```python
for line in linelist:
    if line not in R:
        R.append(line)
```

5.  Open the text file in write mode and write the unique lines in the temporary list to the file:
    

```python
with open("content.txt", "w") as f:
    for line in R:
        f.write(line)
```

This is the complete Python program to find and remove duplicate lines in a large text file. The program first reads the lines of the file into a list, then removes the duplicates from the list and finally writes the unique lines back to the file.

Here is the complete code for the Python Program:

```python
# Opening the Text File in Read Mode
with open("content.txt", "r") as f:
    linelist = f.readlines()

# Temporary List
R = []

# Iterating through the lines and checking for duplicates
for line in linelist:
    if line not in R:
        R.append(line)    

# Writing Unique Lines in Text File
with open("content.txt", "w") as f:
    for line in R:
        f.write(line)
```