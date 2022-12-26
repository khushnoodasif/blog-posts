# Changing the First and Last Letter of a Word in Python

In this tutorial, you will learn how to write a Python program to change the first and last letter of a given word. Let's get started with the code. If you find this article helpful, please consider sharing it with your coding communities and social media groups so that others can benefit from the content as well.

To change the first and last letter of a word, we will follow these steps:

1.  Define the word that we want to modify as a string variable. In this example, we are using the word "Welcome":
    

```python
s = "Welcome"
```

2.  Create an empty string called `r` to store the modified version of the word.
    

```python
r = ""
```

3.  Prompt the user to enter the first and last letters that they want to replace.
    

```python
a = input("Enter first letter to be replaced:- ")
b = input("Enter last letter to be replaced:- ")
```

4.  Concatenate the first letter (entered by the user) to the `r` string.
    

```python
r += a
```

5.  Iterate through the characters in the `s` string, starting at index 1 (to skip the first letter) and ending at the second-to-last index (to skip the last letter). As we iterate through the string, we will concatenate each character to the `r` string.
    

```python
for x in range(1,len(s)):
    r = r + s[x]
```

6.  Concatenate the last letter (entered by the user) to the `r` string.
    

```python
r += b
```

7.  Print out the modified version of the word stored in the `r` string.
    

```python
print(r)
```

Here is the complete code for this program:

```python
s = "Welcome"
r = ""
a = input("Enter first letter to be replaced:- ")
b = input("Enter last letter to be replaced:- ")
r += a
for x in range(1,len(s)):
    r = r + s[x]
r += b
print(r)
```

For example, if the user enters "f" for the first letter and "m" for the last letter, the output will be:

```python
felcomem
```

I hope this code and explanation are helpful in understanding how to change the first and last letter of a word in Python. Thank you for reading!