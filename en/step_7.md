## What is the date?

To know which picture to display behind the door, the program must know what the date is. Python has a built in way of providing you with the current date that you can use.

In the starter file we have already added this line at the top to import the functions `sleep` (for pausing the program) and `strftime` (for getting the current date or time).

```python
from time import sleep, strftime
```

+ Go to the **main** section of your program and create a variable called `day`. Using the `strftime` function, set the value of the variable to be the current day as a number (e.g. 24 if it is the 24th).

[[[generic-python-strftime]]]

+ Repeat these instructions for another variable called `month` which contains the current month name (e.g. "March" or "December").

--- hints ---
--- hint ---
Look up the correct format string for what you want to see in the [strftime reference](http://strftime.org/). For example, if you wanted to get the current day of the week, the format string you would use would be "%A".
--- /hint ---
--- hint ---
Plug in the format string you looked up into the strftime function, between the brackets.

```Python
day = strftime(    )
```
--- /hint ---
--- hint ---
Here is the code you will need:

```python
day = strftime("%d")
month = strftime("%B")
```
--- /hint ---
--- /hints ---

The function `strftime` is short for "string format time", so this means the results you get back are always **strings**.

+ Add code to the line containing your `day` variable to convert the variable into an **integer**. For example if today is the 24th, your variable would contain `"24"` but we actually want it to contain `24`.

```python
day = int(strftime("%d"))
```

--- collapse ---
---
title: Why does this matter?
---
A **string** is a piece of text whereas an **integer** is a whole number. We might want to perform calculations on numbers or compare them to each other.

Let's say we left the `day` as a string and today is the 23rd. If you asked Python to double the number you would expect to get `"46"`.

![String without casting](images/string-cast.gif)

This is because the data is behaving like text - two lots of `"23"` is `"2323"`. If we want the day to behave like an integer, we must convert it to an integer.

--- /collapse ---
