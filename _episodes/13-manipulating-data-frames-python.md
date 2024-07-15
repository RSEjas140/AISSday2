---
title: "Pandas and manipulating data frames"
teaching: 20
exercises: 10
questions:
- "How do I manage tabular data efficiently?"
objectives:
- "Understand how Pandas can be used to store, manipulate and subset tabular data."
keypoints:
- "Pandas provides powerful data structures like Series and DataFrame for easy manipulation and analysis of structured data."
- "It offers extensive functionality for data cleaning, selection, transformation, and integration with other libraries like NumPy and Matplotlib."
- "With Pandas, you can efficiently handle data tasks such as handling missing values, merging datasets, and preparing data for machine learning models."
---

## Inspecting Datasets
Pandas is a Python library for data manipulation and analysis, providing powerful data structures like DataFrame and Series along with a wide range of functions for tasks such as data cleaning, preparation, and exploration. It is widely used in data science and machine learning workflows for its ease of use and flexibility.

We can now explore the Iris dataset to gain insights into its structure and contents.

### Inspecting a Dataset
To understand the structure of the Iris dataset, we can use various methods provided by Pandas:

```
print(iris_df.head())
```
{: .language-python}

```
print(iris_df.info())
```
{: .language-python}

```
print(iris_df.describe())
```
{: .language-python}

```
print(iris_df.columns)
```
{: .language-python}

Understanding the contents and data types of a data set is important for accurate analysis.

### Manipulating DataFrames
Pandas provides powerful functionalities to manipulate DataFrames. Here are some examples:

Adding and Removing Columns

Adding:
```
iris_df['sepal.ratio'] = iris_df['sepal.length'] / iris_df['sepal.width']
```
{: .language-python}

Removing:
```
iris_df.drop('variety', axis=1, inplace=True)
```
{: .language-python}

Adding and removing rows

Adding:
```
new_row = {'sepal.length': 5.1, 'sepal.width': 3.5, 'petal.length': 1.4, 'petal.width': 0.2,}
iris_df.loc[len(iris_df)] = new_row
```
{: .language-python}

Removing:
```
iris_df.drop(0, inplace=True)
iris_df.reset_index(drop=True, inplace=True)
```
{: .language-python}


### Subsetting Data

Subsetting allows us to select specific rows or columns based on conditions:

```
iris_df = pd.read_csv("data/iris.csv") #reset the dataset
# Select rows where petal_length is greater than 5
subset_df = iris_df[iris_df['petal.length'] > 5]
```
{: .language-python}

```
# Select rows where species is 'setosa' and petal_length is less than 1.5
subset_df = iris_df[(iris_df['variety'] == 'Setosa') & (iris_df['petal.length'] < 1.5)]
```
{: .language-python}

```
# Select rows where sepal_length is greater than 5 and species is either 'setosa' or 'versicolor'
subset_df = iris_df[(iris_df['sepal.length'] > 5) & (iris_df['variety'].isin(['Setosa', 'Versicolor']))]
```
{: .language-python}

```
# Select rows where species is 'setosa' or 'versicolor' and petal_length is not equal to 1.5
subset_df = iris_df[(iris_df['variety'].isin(['Setosa', 'Versicolor'])) & (iris_df['petal.length'] != 1.5)]
```
{: .language-python}


### Applying a function

To apply a function to a DataFrame column in Pandas, you can use the .apply() method.

```
# Define a custom function
def square_value(x):
    return x ** 2
```
{: .language-python}

```
iris_df['petal.length.squared'] = iris_df['petal.length'].apply(square_value)
```
{: .language-python}

### Useful organisational tools

* Renaming columns:
```
iris_df.rename(columns={'sepal.length': 'sepal_length'})
```
{: .language-python}


* Setting index: 
```
iris_df.set_index('petal.length.squared')
```
{: .language-python}

### Transformations

* Sorting:

```
iris_df.sort_values(by='sepal_length')
```
{: .language-python}

* Grouping:

```
iris_df.groupby('variety').mean()
```
{: .language-python}

### Filtering
```
df = iris_df[iris_df['petal.legnth'] > 1.1] 
```
{: .language-python}


### Exporting data

Manipulations, transformations, etc. can take time on big datasets. You won't want to repeat this everytime you want to work on your data. So good practice is to save the output as a new file. 

```
iris_df.to_csv("p_data\sensible_name.csv")
```
{: .language-python}


Pandas is highly efficient for DataFrame manipulation due to its intuitive syntax and powerful functionalities. It offers a wide range of built-in functions for data selection, filtering, and transformation, making tasks like data cleaning and preprocessing streamlined. 
