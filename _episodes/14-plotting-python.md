---
title: "Plotting in Python with Matplotlib"
teaching: 15
exercises: 15
questions:
- "How do I create plots?"
- "How do I use data sets to populate my plot?"
objectives:
- "Understand how plots are formed syntactically in Matplotlib."
- "Can create plots from data sets."
keypoints:
- "Plotting is a useful tool for understanding our data; it is not just for results visualization."
---

## Plotting

Plotting our data is one of the best ways to intuitively explore it, and the various relationships between variables. While there are several libraries available for plotting in Python, we'll be using Matplotlib because it is versatile and widely used. Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. Let's start by exploring a simple example using Matplotlib in Python. Make sure you have Matplotlib installed in your Python environment:

```
pip install matplotlib
import matplotlib.pyplot as plt
```
{: .language-python}


```
#simple plot
plt.figure()
plt.plot(x,y)
plt.show()
```
{: .language-python}

```
#less simple plot
plt.figure()
plt.scatter(iris_df['sepal.length'], iris_df['sepal.width'])
plt.xlabel('Sepal Length (cm)')
plt.ylabel('Sepal Width (cm)')
plt.title('Sepal Length vs Sepal Width')
plt.show()
```
{: .language-python}

## Plot Types

* Line Plot: 
```
plt.figure()
plt.plot(iris_df.index, iris_df['sepal.width'])
plt.xlabel('Item number')
plt.ylabel('Sepal Width (cm)')
plt.title('Sepal Widths')
plt.show()
```
{: .language-python}

* Bar Plot: 
```
#modify data for bar plot
species_counts = iris_df['variety'].value_counts()

plt.figure()
plt.bar(species_counts.index, species_counts.values)
plt.title('Number of Samples for Each Iris Species')
plt.xlabel('Species')
plt.ylabel('Count')
plt.show()
```
{: .language-python}
* Histogram: 
```
plt.figure()
plt.hist(iris_df['sepal.length'], bins=20)
plt.title('Histogram of Sepal Length')
plt.xlabel('Sepal Length (cm)')
plt.ylabel('Frequency')
plt.show()
```
{: .language-python}

### Other plots

* Box Plot: 
```
plt.boxplot(data)
```
{: .language-python}
* Pie Chart: 
```
plt.pie(sizes, labels=labels)
```
{: .language-python}
* Heatmap: 
```
plt.imshow(data, cmap='hot', interpolation='nearest')
```
{: .language-python}

### More options

Add legend: 
```
plt.figure()
plt.plot(iris_df.index, iris_df['sepal.width'], label = 'Width')
plt.plot(iris_df.index, iris_df['sepal.length'],label = 'Length')
plt.xlabel('Item number')
plt.ylabel('Sepal Width and length (cm)')
plt.title('Sepal Widths')
plt.legend()
plt.show()
```
{: .language-python}

Annotations: 
```
plt.annotate('text', xy=(x, y))
```
{: .language-python}

## Improving plots aesthetically

Figures can be saved in .svg format and edited in graphic software like inkscape. Some minor changes to display options can improve the lok of a visualisation (depending on your taste). 

```
plt.figure(figsize=(10, 6)) #custom figure size
plt.hist(iris_df['sepal.length'], bins=20, color='skyblue', edgecolor='black') # colour choices
plt.title('Histogram of Sepal Length')
plt.xlabel('Sepal Length (cm)')
plt.ylabel('Frequency')
plt.grid(True, linestyle='--', alpha=0.75) #alpha grid
plt.show()
```
{: .language-python}

## Saviing (for multiple plots)
```
plt.savefig('filename.png') #.pdf .svg
```
{: .language-python}

As you have seen there are many different type of plots, if you need a specific kind of plot a good place to start is the super helpful cheat sheets on Matplotlib below. 


[Plotting in Matplotlib cheat sheet](https://images.datacamp.com/image/upload/v1676360378/Marketing/Blog/Matplotlib_Cheat_Sheet.pdf)  
[Matplotlib cheat sheet](https://matplotlib.org/cheatsheets/cheatsheets.pdf)


