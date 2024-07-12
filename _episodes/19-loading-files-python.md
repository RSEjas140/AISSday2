---
title: "Loading data into Python using Spyder"
teaching: 5
exercises: 5
questions:
- "How do I load my own data into Spyder?"
objectives:
- "Can load data files into Spyder."
keypoints:
- "Loading in the data is just the first step"
---

### Loading your data
Getting your data into Python using Spyder is the first step to doing something interesting with it. Click both links below to download both datasets.

[Download File](../fig/gapminder_data.csv)  

[Download File](../fig/iris.csv)

Place them in a folder (name the folder ‘data’) and change the file permissions of the dataset to read-only. The easiest way to achieve this is to find the document in your file management system, inspect its properties, and apply read-only.

>Note: You can also do this through the command line using ‘attrib +r’ for windows or ‘chomd 444’ for linux/mac. 
>This is only recommended if you have prior experience working in the command line.

To load our file, in the console, type:

```
pip install pandas # if you have not installed pandas before
import pandas as pd
```
{: .language-python}

### Load the Iris dataset
```
iris_df = pd.read_csv("data/iris.csv") #depending on os and project setup
```
{: .language-python}

This is a simple introduction to getting your data into Python using Spyder. In some cases, there will be significant complications (e.g., many files, large data size, unusual file format, etc.). In cases like this, Python libraries such as glob, pathlib and pandas have tools to help.

