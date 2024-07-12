---
title: "Variables and assignment"
teaching: 15
exercises: 5
questions:
 - "What can we store in variables?"
 - "What is good practice for variable naming?"
 - "What can I do with variables?"
objectives:
 - "Confident assigning variables"
 - "Understand different data types"
keypoints:
 - "When naming variables it's important be consistent and succinct"
 - "Output assignment has to be explicit to keep the result of an operation"
 - "Python may make assumptions about data types unless you are explicit"
---

### What are variables and why do we want them?
We don’t just want Spyder to be our calculator. We want to be able to store and manipulate data in a meaningful way. We want to perform operations on data, possibly many times. It would be useful to have a clarity and context for the data we are using; ideally descriptive names to make our data more manageable.

### Data types 
Python utilises different data types to efficiently store and manipulate different kinds of data. Python is dynamical typed; this means that you do not need to specify a data type when you declare a variable. You can give the variable name and the data you want to store and let Python worry about how it deals with that. We will look at the most common data types in Python.
  
| Data Type       | Description                                     | Example                     |
|-----------------|-------------------------------------------------|-----------------------------|
| int             | Integer data type                               | 42                          |
| float           | Floating-point data type                        | 3.14                        |
| str             | String data type                                | 'hello'                     |
| bool            | Boolean data type                               | True, False                 |
| NoneType        | NoneType data type (represents null value)      | None                        |
  
  
### Defining variables
Let's go ahead and define some variables. Into the console type:  

```
x = 10
```
{: .language-python}  

```
y = 5
```
{: .language-python}


The variables x and y should now have populated your variable explorer tab. We can inspect them, but they are relatively predictable. 

### Delcare more variables:
Let's add a few other variables of different variable types, Try:

```
my_name = "your name"
```
{: .language-python}

```
likes_rstudio = TRUE
```
{: .language-python}
  

Now we have created some variables we can try refering to them in the console. Type:  

```
x + 5
```
{: .language-python}

```
15
```
{: .output}


> ## What does the variable explorer say about variable x?
> You should notice that the variable 'x' has not changed it's value to 15.
{: .challenge}

Now try:
```
x = x + 5
```
{: .language-python}

When you check the variable again in the variable explorer tab you should now notice that it is 15. This is a key concept to recognise; we can perform an operation and the resulting output will be shown but unless we explicitly assign it the change will not be saved.

## Variable naming

Variable naming is important but often overlooked by new programmers (and experienced programmers). It is not trivial to think of meaningful concise variable names. The first thing to understand is that Python has some restrictions and rules for variable naming:  

 
* Variable names are cases sensitive (My_name is different to my_name).  

* They must start with a letter or a underscore. 

* They can consist of letters, numbers, periods, and underscores.  

* There are reserved words (e.g., ‘else’, ‘for’) that cannot be used for naming variables as they are already used by Python for specific purposes.  

 
It may seem fussy but there are actually not that many enforced restrictions compared to the number of variable naming combinations. However, just because you can, doesn’t mean you should. There exist several naming conventions in the Python community to help provide structure and guidance to variable naming. 

 

1. my_variable (underscore or snake case) 

2. myVariable (camel case) 

 

Although some may disagree with us, we believe for most users it does not matter which convention you pick. There are two key principles for variable naming, that we recommend, that should make your life easier: 

 

1. ***Consistency*** – pick a convention and stick with it. 

2. ***Succinctness*** - Keep variable names short, readable, and descriptive. 

 

For ***example***, if you wanted a variable name for a temperature reading taken in Aberystwyth: 


This: 

>min_temp_aber_C 


Is better than this: 

>temp 
 

Or this: 

>themininimumtemperaturerecordedfromaberystwythindegreescelcius 

 
Being consistent, aware of context, and conscious of your variable naming will make reading your code easier and decrease the risk of errors.   

>## Useful tool
>* ***type***  
>You can datatype information using type() on your variables.  
{: .callout}

```
type(x)
```
{: .language-python}

```
"int"
```
{: .output}


Python provides built-in functions like int(), float(), str() so you can cast variables to different types.

```
x = str(x)
```
{: .language-python}


```
type(x)
```
{: .language-python}

```
str
```
{: .output}

```
x
```
{: .language-python}

```
'5'
```

### Summary

Most of the time data types will not be of great concern to you. However, it is worth remembering that when you ask Pyton to read and organise data, unless you are explicity, you are asking it to make assumptions on the data types.
