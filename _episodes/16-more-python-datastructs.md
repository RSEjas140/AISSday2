---
title: "Lists and dictionaries in Python"
teaching: 15
exercises: 5
questions:
- "What other data structures are there?"
objectives:
- "Understand the use of lists and dictionaries in Python."
keypoints:
- "Dictionaries: Efficient for fast key-based retrieval and storing data with unique identifiers."
- "Lists: Versatile collections for storing ordered heterogeneous data types with various operations like indexing and appending."
---

## Lists

- Lists are ordered collections of items, which can be of any data type.
- They are mutable, meaning their elements can be changed after creation.
- Lists are created using square brackets \[\].

Example of list creation:
```
my_list = [1, 2, 3, 'apple', 'banana', 'cherry']
```
{: .language-python}

### Indexing and accessing elements:
- Elements in a list are accessed using square brackets \[\] and indices (e.g. my_list\[4\]).
- Indexing starts from 0 for the first element.

```
last_element = my_list[-1]   # Accessing the last element
```
{: .language-python}


### Manipulating lists:
- Lists support various operations like adding, removing, and updating elements.

Examples of manipulation:
```
my_list.append('orange')     # Adds 'orange' to the end of the list
my_list.insert(2, 'pear')    # Inserts 'pear' at index 2
my_list.remove('banana')     # Removes the first occurrence of 'banana'
my_list.pop()                # Removes and returns the last element
my_list[0] = 'grape'         # Updates the first element to 'grape'
```
{: .language-python}

## Dictionaries

- Dictionaries are unordered collections of key-value pairs.
- They are mutable and can contain keys of any immutable data type.
- Dictionaries are created using curly braces \{\}.

Example of dictionary creation:
```
my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}
```
{: .language-python}

### Accessing elements:
- Elements in a dictionary are accessed using square brackets \[\] and keys.

Example of accessing elements:
```
person_name = my_dict['name']   # Accessing value corresponding to 'name' key
```
{: .language-python}

### Manipulating dictionaries:
- Dictionaries support various operations like adding, removing, and updating key-value pairs.

Examples of manipulation:
```
my_dict['gender'] = 'Male'     # Adds 'gender': 'Male' to the dictionary
del my_dict['age']             # Removes the key 'age' and its value
my_dict['city'] = 'Los Angeles' # Updates the value of 'city' key to 'Los Angeles'
```
{: .language-python}

