# Determining the Number of Days in a Month with Python

Have you ever needed to know how many days are in a particular month? Python makes it easy to find out with just a few lines of code.

First, we start by asking the user to enter the name of the month they are interested in.

```python
month = input("Enter Month")
```

Next, we use an `if` statement to check if the month the user entered is one of the months that has 31 days. We do this by creating a tuple of month names that have 31 days and using the `in` operator to check if the user's input is in that tuple. If it is, we print a message saying that the month has 31 days.

```python
if month.lower() in ("january,march,may,july,august,october, december"):
    print("It has 31 Days")
```

Then, we use an `elif` statement to check for the special case of February. February can have either 28 or 29 days, depending on whether it is a leap year or not. So, we print a message saying that February has either 28 or 29 days depending on the year.

```python
elif month == "february":
    print("It has 28 in a non Leap year and 29 Days in a Leap year")
```

Finally, we use an `else` statement to handle the remaining months, which are all the ones that have 30 days. We print a message saying that these months have 30 days.

```python
else:
    print("It has 30 Days")
```

And that's it! With just a few lines of code, we can easily determine how many days are in any given month. You could even take it a step further and ask the user for the current year, and use that information to determine the number of days in February for a leap year.

I hope this helps clarify the logic and flow of the code for finding the number of days in a month with Python.