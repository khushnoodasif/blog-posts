# Count Number Of Uppercase, Lowercase, Space In A Text File

Write a Python function `count_characters()` to count the number of uppercase, lowercase, digits, spaces, and special characters in a text file.

## **Logic and Explanation**

In this problem, we need to iterate through all the characters in a text file and count the number of uppercase, lowercase, digits, spaces, and special characters.

First, we will create variables to hold the count for each category. Then, we will open the text file using the following command:

```python
with open(file_name, 'r') as f:
```

Next, we will iterate through the file and read it character by character. For each character, we will check its category (uppercase, lowercase, digit, space, or special character) and increase the count for that category.

For example, to check for uppercase characters, we can use the following code:

```python
if c.isupper():
    uppercase_count += 1
```

We can use similar code to check for the other categories.

To help understand the logic, you can add debugging statements to print the values of the variables at each step.

I hope the logic for this problem is now clear. You are encouraged to try implementing it on your own before checking the source code below.

## **Source Code**

```python
def count_characters(file_name):
    uppercase_count = lowercase_count = digit_count = space_count = special_count = 0
    
    with open(file_name, 'r') as f:
        for line in f:
            for c in line:
                if c.isupper():
                    uppercase_count += 1
                elif c.islower():
                    lowercase_count += 1
                elif c.isdigit():
                    digit_count += 1
                elif c.isspace():
                    space_count += 1
                else:
                    special_count += 1
    
    print("Number of uppercase characters:", uppercase_count)
    print("Number of lowercase characters:", lowercase_count)
    print("Number of digits:", digit_count)
    print("Number of spaces:", space_count)
    print("Number of special characters:", special_count)
```

## **Usage**

To use the `count_characters()` function, pass in the file name as a string argument:

```python
count_characters("story.txt")
```