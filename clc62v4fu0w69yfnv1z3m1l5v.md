# Separating Numbers and Letters from a String in Python

In this tutorial, you will learn how to write a Python program to separate the numbers and letters from a given string. Let's get started with the code. If you find this article helpful, please consider sharing it with your coding communities and social media groups so that others can benefit from the content as well.

To separate the numbers and letters from a string, we will follow these steps:

1.  Define the string that we want to process and two empty strings called `n` and `a` to store the numbers and letters, respectively. In this example, we are using the string "He1l3lo56":
    

```python
s = "He1l3lo56"
n = a = ""
```

2.  Iterate through the characters in the `s` string. For each character, use the `isdigit()` method to check if it is a number. If it is a number, concatenate it to the `n` string. If it is not a number, use the `isletter()` method to check if it is a letter. If it is a letter, concatenate it to the `a` string.
    

```python
for x in s:
    if x.isdigit():
        n += x
    if x.isletter():
        a += x
```

3.  Print out the `n` and `a` strings to see the separated numbers and letters.
    

```python
print("Numbers in string=", n)
print("Letters in string=", a)
```

Here is the complete code for this program:

```python
s = "He1l3lo56"
n = a = ""
for x in s:
    if x.isdigit():
        n += x
    if x.isalpha():
        a += x
print("Numbers in string=", n)
print("Letters in string=", a)
```

Running this code will result in the following output:

```python
Numbers in string= 1356
Letters in string= Hello
```

I hope this code and explanation are helpful in understanding how to separate the numbers and letters from a string in Python. Thank you for reading!