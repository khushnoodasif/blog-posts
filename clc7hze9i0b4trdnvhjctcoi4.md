# Searching for Python Files in a Folder: A Step-by-Step Guide

To search for py files in a folder, we can use the `os` module in Python. First, we will import the `os` module at the top of our Python file.

```python
import os
```

Next, we will define the path of the folder in which we want to search for py files. In this example, we will search for py files in a folder called `Python Programs` located in the current working directory.

```python
path = './Python Programs/'
```

Then, we will use the `os.listdir` function to get a list of all the files and folders in the specified directory.

```python
files = os.listdir(path)
```

To filter out only the files from the list of files and folders, we can use the `os.path.isfile` function. This function takes in the path of a file or folder and returns `True` if it is a file, and `False` if it is a folder.

```python
files = [f for f in files if os.path.isfile(os.path.join(path, f))]
```

Now that we have a list of only the files in the specified directory, we can iterate through the list and check if the file has a `.py` extension. To do this, we will split the file name at the `.` character and check if the second element in the resulting list is equal to `'py'`. If it is, we will print the file name.

```python
for file in files:
    file_parts = file.split('.')
    if file_parts[1] == 'py':
        print(file)
```

Here is the complete Python code for searching for py files in a folder:

```python
import os

Directory of the folder in which we have to search for py files
path = './Python Programs/'

for file in os.listdir(path):
# Check if the current file is a file (not a folder)
if os.path.isfile(os.path.join(path, file)):
# Split the file name at the '.' character to separate the name and extension
file_name_parts = file.split(".")
# If the second part (the extension) is 'py', print the file name
if file_name_parts[1] == "py":
print(file)
```

And that's it! You should now have a working Python program that can search for .py files within a specific folder. Give it a try and see if it works for you. Happy coding!