---
title: "Functions"
teaching: 15
exercises: 5
questions:
- "How do I make my own functions?"
- "Why would I want to make my own functions?" 
objectives:
- "Understand function structure"
- "Confident declaring custom functions"
keypoints:
- "Functions can help reduce redundancy and increase reusability in your code"
---

### Exploring functions

So far, we have just been using functions without exploring what they are doing. For example, you type `math.sqrt()` and place your value (argument/parameters) into the function, some magic happens, and it returns an output. We will now start to explore the structure of functions and how we can create our own.  

### Function Structure

```python
def function_name(parameter1, parameter2, ...):
    """Description of the function."""
    # Function body
    return result
```

- **def**: Keyword to define a function.
- **function_name**: Name of the function.
- **(parameter1, parameter2, ...)**: Parameters (optional).
- **Description**: Brief function description for users (not used by Python).
- **return**: Keyword to return a value (optional).
- **result**: Value to be returned (optional).

### Function example

We can convert our previous calculation into a function. Open a new script file and type this in: 

```python
def celc_to_fahr(celc):
    fahr = celc * 9/5 + 32
    return fahr
```

Save this script as 'my_functions' and run it.

Now we can convert Celsius to Fahrenheit in the console by typing:

```
celc_to_fahr(14) 
```
{: .language-python}
```
57.2
```
{: .output}

Go back to to the script my_first_script. At the top of the script place this line:

```
import my_functions as mf
```
{: .language-python}

```
mf.celc_to_fahr(14) 
```
{: .language-python}

We can now run this function from my_first_script.

Wherever significant duplication exists in your code, it's advisable to create a function to replace it. This approach promotes code reusability, readability, and maintainability. If you have generalised functions that you use often in different scripts, it is good practice to store them in a script file. You can then import them into any project that you need them for. This reduces rewriting and editing code, and decreases the chance of introducing errors such as typos or calculation errors.

