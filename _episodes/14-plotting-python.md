---
title: "Plotting in Python with Matplotlib"
teaching: 10
exercises: 5
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
plt.figure(figsize=(8, 6))
plt.scatter(iris_df['sepal.length'], iris_df['sepal.width'])
plt.xlabel('Sepal Length (cm)')
plt.ylabel('Sepal Width (cm)')
plt.title('Sepal Length vs Sepal Width')
plt.show()
```
{: .language-python}

To give you more freedom you can plot into a seperate window.

1. Go to the "Tools" menu and select "Preferences" (on Windows/Linux) or "Spyder" menu and select "Preferences" (on macOS).
2. In the Preferences dialog, navigate to the "IPython console" section.
3. Click on the "Graphics" tab.
4. Make sure that the "Inline backend" option is unchecked.

### More plotting

There are many different type of plots, if you need a specific kind of plot a good place to start is the super helpful cheat sheet on Matplotlib. To explore all the different options you can to these cheat sheets:


[Plotting in Matplotlib cheat sheet](https://images.datacamp.com/image/upload/v1676360378/Marketing/Blog/Matplotlib_Cheat_Sheet.pdf)  
[Matplotlib cheat sheet](https://matplotlib.org/cheatsheets/cheatsheets.pdf)


