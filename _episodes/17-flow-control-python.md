---
title: "Flow control"
teaching: 25
exercises: 5
questions:
- "How do we get our code to react dynamically?"
- "How do we delegate repetitive tasks and decisions?"
- "How do we make our software robust to a wider set of use cases?"
objectives:
- "Understand the role of flow control in managing the order of statement execution."
- "Understand the role how to combine conditional, logical, and comparison operators in Python."
keypoints:
- "Flow control is an important technique you need to learn to create useful software."
- "Simplicity is often the best option whenever possible."
- "Plan and refactor your code regularly."
---

Often, we want to perform different operations in our code based upon dynamic conditions. To explore this idea, we are going to pretend we have two sensors. The first representing a temperature, and the second representing if there is rainfall. Our temperature is a numeric value, and our rainfall is a boolean. To declare those variables, type into the script:

```
temp_reading = 16 

rainfall = True 
```
{: .languge.python}
Then place the following code into your script:

```
if rainfall == True: 
  print("Advise user to take an umbrella") 
```
{: .languge.python}

Run the script using the run button (little green play button) above the script pane.

```
"Advise user to take an umbrella"
```
{: .output}

From observing the output in the console and from a brief inspection of the code, it should be evident that we are evaluating the variable rainfall. Specifically, we are checking if it is True. If the outcome is of the check is valid, then we perform any code within the indented block.

{% include figure.html max-width="100%" file="/fig/ifflow1.png" 
alt="Flow diagrame for if condition" caption="Figure 1: Flow diagram for an *if* condition" %}


### if, else

Now modify your code to look like this:

```
if rainfall: 
  print("Advise user to take an umbrella") 
else: 
  print("Leave your umbrella at home") 
```
{: .languge.python}

Note: With boolean variables, we don't actually have to check for equivalence.

{% include figure.html max-width="100%" file="/fig/ifflow2.png" 
alt="Flow diagrame for if condition" caption="Figure 2: Flow diagram for an if, else condition" %}

### Change the condition
Now change the rainfall variable to False and run the script again.

```
rainfall = False
```
{: .languge.python}

```
"Leave your umbrella at home"
```
{: .output}

Our code now reacts differently to different input values. You can combine if, elif (else if), and else statements to control the flow of your code.

### Conditional statements
- 'if' – Used to execute a block of code if a condition is true.
- 'elif' – Extends an 'if' statement to check a condition only if the previous 'if' or 'elif' condition was resolved as false.
- 'else' – Extends an 'if' statement, will execute if none of the preceding 'if' conditions are true.

### Comparison operators
We have encountered '==', which is used to check for equivalence. There are other comparison operators available to us.
- \> Greater than
- \>= Greater than or equal to
- < Less than
- <= Less than or equal to
- == Equal to
- != Not equal to

### Boolean operators

* **and**: The and operator returns True if both operands are True, otherwise it returns False.
* **or**: The or operator returns True if at least one of the operands is True, otherwise it returns False. 
* **not**: The not operator returns True if the operand is False, and False if the operand is True. 

Replace the code in your script with this (keeping the variables):

```
if rainfall or temp_reading < 10:
    print("Stay at home") 
else:
    print("Go outside")
```
{: .languge.python}

By combining these operators, you can create sophisticated flow control mechanisms.

### For loops

In Python, a for loop is used to iterate over a sequence and perform a set of statements for each item in the sequence. Here's how a for loop works in Python:

1. **Syntax:** The syntax of a for loop in Python is as follows:
   
   ```python
   for item in sequence:
       # Statements to execute for each item
   ```

2. **Explanation:** 
   - The `for` keyword is used to start the loop.
   - `item` is a variable that takes each value from the `sequence` in each iteration of the loop.
   - `sequence` is the collection of items over which the loop iterates.
   - Indentation is used to define the block of statements to be executed for each iteration of the loop.   


3. **Examples:** Here's an examples of a for loop that iterates over a range of numbers and prints each number:
   
```
   for i in range(5):
       print(i)
```
{: .languge.python}

```
0
1
2
3
4
```
{: .output}

 Here's an examples of a for loop that iterates over a list of strings and prints each string:

```
days = ['monday','tuesday','wednesday','thursday','friday']

for day in days:
    print(day)
```
{: .languge.python}
  
```
monday
tuesday
wednesday
thursday
friday
```
{: .output}

For loops are commonly used in Python for iterating over sequences, performing repetitive tasks, and processing collections of data.

### Keeping things clear
It is possible to put conditional statements inside conditional statements these are then referred to as 'nested'. If your code becomes overly nested it can impact readability and maintainability. It is good practice to keep your workflow as simple as possible, this can be made easier by spending time on design and regular refactoring.

Note: Refactoring is the process of restructuring code, not to change the functionality but to improve factors like readability, maintainability, efficiency.

We've covered a very basic introduction to flow control in Python, but there are many more facets to explore in order to fully understand all possibilities. Please feel free to check out the link below for more information on flow control.

[More flow control in Python](https://docs.python.org/3/tutorial/controlflow.html)
