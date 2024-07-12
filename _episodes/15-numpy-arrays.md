---
title: "Arrays and vectorisation with NumPy"
teaching: 15
exercises: 5
questions:
- "How do we manage many variables efficiently?"
objectives:
- "Be able to declare, manipulate, and address arrays."
- "Understand the process and role of vectorisation with NumPy."
keypoints:
- "By default arrays hold elements of the same data types."
- "Vectorisation with NumPy allows us to apply operations to all the elements in an array efficiently."
- "Arrays can be indexed using various methods to retrieve/manipulate the specific information you desire."
---

### What happens when we have to deal with multiple variables?

It may have occurred to you that dealing with variables individually is going to be less and less efficient as our data size set gets significantly larger. We are going to explore how we can store and organize our data in some useful ways.

### Arrays 

Arrays are multi-dimensional collections of items, commonly used in numerical computing. We can declare an array in the console using NumPy like this:

```
pip install numpy #if you don't have numpy installed already
```
{: .languge.python}
```
import numpy as np
```
{: .languge.python}

```
temperatures = np.array([23.5, 20.6, 15.8, 22.0])
```
{: .languge.python}


You can also create arrays using other methods provided by NumPy. Now try: 

```
num_range = np.arange(1, 11) 
```
{: .languge.python}

```
num_rep = np.full(10, 1) 
```
{: .languge.python}

```
num_sequence = np.linspace(0, 1, num=11)
```
{: .languge.python}

Congratulations, we now have four arrays. Are they what you were expecting? Type the variable names into the console to get an output of their contents.

Can you determine how each one works?
1. np.arange()
2. np.full() 
3. np.linspace()

You can always look them up using the NumPy documentation if you are not sure.

### Addressing and manipulating arrays

Once created, it is possible we may want to modify the elements in our array.

You can address positions in the array using the syntax 'array[index]', for example:

```
temperatures[0]
```
{: .languge.python}


If we want to change what is at that index we can type:

```
temperatures[0] = 20.5
```
{: .languge.python}

**Be aware Python indexing starts at 0.**

We can access the last item in the array using:
```
temperatures[-1]
```
{: .languge.python}


### Vectorisation with NumPy

We can perform mathematical operations on arrays efficiently using NumPy functions:

```
np.mean(temperatures) 

np.sum(temperatures) 

np.min(temperatures) 

np.max(temperatures) 

np.round(temperatures) 
```
{: .languge.python}


Notice that for rounding we did not have to explicitly ask for each calculation on each element to be performed. NumPy allows us to apply the same operations we can apply to a single element to arrays directly. This is called vectorisation.

We may want to apply an operation that does not exist as an in-built function, Try: 

```
temperatures = temperatures * 9/5 + 32 
```
{: .languge.python}

We have explicitly told Python to save the output back into the 'temperatures' array. All the temperatures have been converted from Celsius to Fahrenheit.

### Make changes but only to specific elements

Sometimes we may only want to change certain elements in an array based on their value. 
Example: Find all the elements that are higher than 70 Fahrenheit and increase them by 10.  
First we need to find out which elements fit our requirement  

```
above_70 = temperatures > 70 
```
{: .languge.python}

This has created a logical array that indicates if that element is above 70 using True/False. You can now use this array to address the 'temperatures' array, selecting only those elements. Try:

```
temperatures[above_70] += 10 
```
{: .languge.python}

Notice '+=' this is the equivalent with temperatures[above_70] = temperatures[above_70] + 10.

This is an example of how we can modify arrays but there are many different ways to address and manipulate arrays based on your required output.