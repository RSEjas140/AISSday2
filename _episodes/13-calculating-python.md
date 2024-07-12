---
title: "Calculating in Spyder"
teaching: 5
exercises: 5
questions:
- "How do we process mathematical operations in Spyder?"
objectives:
- "Become familiar with mathematical operators and in-built functions in Spyder."
- "Become confident using the console to run mathematical operations."
- "Understand the order of operations."
keypoints:
- "***PEDMAS***"
- "Use mathematical functions, you don't need to reinvent the wheel."
---

### Dipping our toes
We have covered some relatively dry theory so let’s take some small steps and start interacting with Python. From the console we can start exploring calculation. Write in the following commands:

```
10 – 5 #(subtraction) 
```
{: .language-python}

```
5
```
{: .output}



```
10 + 5 #(addition) 
```
{: .language-python}

```
15
```
{: .output}



```
10 * 5 #(multiplication) 
```
{: .language-python}
```
50
```
{: .output}



```
10 / 5 #(division) 
```
{: .language-python}

```
2
```
{: .output}



```
5 ** 2 #(exponentiation) 
```
{: .language-python}
```
25
```
{: .output}



```
10 % 3 #(modulus)  
```
{: .language-python}
```
1
```
{: .output}

Note: anything following a '#' is considered a comment. Comments are not read by Python they are just used to inform users.


### Order of operations

> ## Question: Before you enter the next calculation, take a second and consider what answer would you be expecting?
```
6 + 9 / 3 
```
{: .language-python}
{: .challenge }


```
9
```
{: .output}


If the answer was **not** what you were expecting you will need to become clear on order of operations in Python. 

 
### Remember **PE(DM)(AS)** 

* **P**arentheses 

* **E**xponentiation 

* **D**ivision/**M**ultiplication\*  

* **A**ddition/**S**ubtraction\*  

\* Operators with same precedent are calculated left to right. 

 
This tells you what order mathematical operations will be performed and ensures consistency during evaluation.  

To make this concept clearer, try: 

```
(6 + 9) / 3 
```
{: .language-python}

```
5
```
{: .output}

Using brackets we have manipulated the order of operations to perform the addition before the division. Be conscious of how you structure your mathematical operations to ensure the desired results but also readability of your code. 

### Mathematical Functions

Combining the math package and build in functions from Python you have a good range of mathematical functions. If you need a fairly common operation there is a good chance it already exists in a package. Let's look at a few examples, try:

```
import math 
```
{: .language-python}
```
math.sqrt(9) 
```
{: .language-python}
```
3
```
{: .output}

```
abs(-5) 
```
{: .language-python}
```
5
```
{: .output}

```
round(3.4) 
```
{: .language-python}
```
3
```
{: .output}

```
math.sin(1)
```
{: .language-python}
```
0.8414709848078965
```
{: .output}


There are a whole range of in-built functions and additional functions available from packages. It is awlays good practice to perform a google search to discover if the function you want already exists.

