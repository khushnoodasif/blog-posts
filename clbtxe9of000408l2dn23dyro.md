# Reading a Text File Word by Word in Python

In this example, we will go over the steps to read lines from a text file and then check for a condition to print out only the words starting with the letter "s".

First, we will open the text file in read mode in our Python program. In this example, we are using a text file called "content.txt" which is located in the same directory as the Python file. To open the file, we can simply use the file name, or provide the complete path if the file is located elsewhere. Here is the code to open the file in read mode:

```python
f = open("content.txt","r")
```

Next, we will read the contents of the file by iterating through the content word by word. To do this, we will first read the entire text file as a string using the `f.read()` function and store it in a string variable called `data`.

```python
data = f.read()
```

Now, we can iterate through the data string by splitting it into words using the `split()` function. By default, this function will split the string on spaces, but we can also specify a different delimiter if needed. Here is the code to iterate through the data string word by word:

```python
for word in data.split():
```

Now, we will check for the condition to only print out words that start with the letter "s". To do this, we will access the first letter of the word using index zero, lowercase it, and then check if it is equal to the lowercase letter "s". If it is, we will print out the word. Here is the code for this check:

```python
if word[0].lower() == "s":
    print(word)
```

Here is the complete source code for this problem:

```python
f = open("content.txt","r")
data = f.read()
for word in data.split():
    if word[0].lower() == "s":
        print(word)
```

For example, the content in the "content.txt" file is:

```python
Hello everyone
My name is Khushnood Asif
Like the post
Subscribe my Youtube channel
Share the content
Thanks for coming
```

Running the above program will result in the following output:

```python
Subscribe
Share
```

I hope the explanation and logic of this program are clear to you. If you have any questions, feel free to ask in the comments below. Thank you for reading!