# Python Program to check Prime Number



The program we will be creating will determine whether a number is a prime number or not. In this case, we will ask the user for a number he wishes to check for prime number.

# Explanation

We'll loop and divide the number with all the numbers less than that number except 1. If any number divides it completely without leaving a remainder, then it is not a prime number, and if it cannot be divided, then it is a prime number.

## Source Code

```bash
n= int(input("Enter a number "))
for x in range(2,n):
    if n%x==0:
        break
if x+1==n:
    print (n,"is a prime number")
else:
    print (n,"is not a prime number")
```


## Output

```bash
Enter a number 1523
1523 is a prime number
```