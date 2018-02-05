# 4-Inputs

## Collecting User Input in Python
A necessary part of making a program interactive is being able to collect information from the user. Collected information is stored in a variable until needed; like this:
```
response = input()
```
Whatever the user types before pressing enter will be stored in the variable "response". The `input()` function always returns a string value, so you'll need to check it and convert it before trying to do math with it. See further below.

You can use the `input()` function to write a prompt for the user too, like this: 
```
response = input("What is your favourite colour? ")
```
Notice the space at the end of the prompt string. This is to make the input look pretty, as you can see by testing it out.

## Converting User Inputs
An important rule in programming is never to believe the user. You have to plan on them doing the wrong thing at all times. An example of this is if we are writing a calculator program. When we ask the user for a number, we have to take into account that they might enter a letter. Also, even if they do enter a number, Python will store it in a String variable, so we will have to convert it anyway.

The term for converting a variable is called casting. We will be casting our string type input to a float type variable for doing calculations. Casting looks like this:
```
response = input("Enter a number to be multiplied >>>")
floatResponse = float(response)
```
If the user inputs a letter the script will crash, but that's ok, we'll learn how to check inputs later.

Recall that we can only concatenate (combine) string variables when we print. So if you convert an input into a number (float or int) you will need to convert it back to a string to print it out; like this:
```
multipliedNumber = floatResponse * 5
strOutput = str( multipliedNumber )
print( "Your number times 5 is " + strOutput )
```
Or you can just use `format()`, like this:
```
multipliedNumber = floatResponse * 5
print( "Your number times 5 is {}".format(multipliedNumber) )
```
Your Tasks:
1.  Use `input()` to collect the user's name and print a personalized greeting statement for them.
2.  Use `input()` to collect the user's name and grade, and then print how many years until they graduate from school.
3.  Use `input()` to collect the user's name and birthdate, and tell them how many days they have been alive. Use `format()` to give them the answer. Hint: you can use multiple prompts to collect the day, month, and year of their birthdate in separate numbers.
```
#Be sure to comment the steps of your code!
```
