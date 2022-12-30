# Python Program to Reverse Each Word in a Text File

Have you ever needed to reverse the order of the words in a text file? In this tutorial, we will show you how to do just that using Python.

We will start by opening the text file in read mode and storing the contents in a string variable called "data". Then, we will iterate through the string, word by word, and reverse each word using string slicing. We will store the reversed words in a new string called "new\_data". Finally, we will overwrite the contents of the text file with the "new\_data" string.

Let's dive into the code:

```python
# Open the text file in read mode and store the contents in a string
with open("demo.txt", "r") as f:
    data = f.read()

# Initialize an empty string for the reversed words
new_data = ""

# Iterate through the data string, word by word
for word in data.split():
    # Reverse the word using string slicing
    rev_word = word[::-1]
    # Concatenate the reversed word to the new_data string
    new_data += rev_word
    # Add a space between each word
    new_data += " "

# Open the text file in write mode to overwrite the contents
with open("demo.txt","w") as f:
    f.write(new_data)
```

In this tutorial, we learned how to reverse each word in a text file using Python. We opened the text file in read mode, iterated through the contents word by word, reversed each word using string slicing, and then overwrote the contents of the text file with the reversed words. I hope the logic and code behind each step is clear to you. If you have any questions, feel free to ask in the comments section below.