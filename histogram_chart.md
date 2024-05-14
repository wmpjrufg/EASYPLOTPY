---
layout: default
title: histogram_chart
parent: Charts
nav_order: 1
has_toc: false
---

<h3>histogram_chart</h3>

<br>

<p align = "justify">
    This function shows a Boxplot and Histogram in a single chart.


</p>

```python
histogram_chart(**kwargs)
```

Input variables
{: .label .label-yellow }

<table style = "width:100%">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
        <th>Type</th>
      </tr>
    </thead>
    <tr>
        <td><code>plot_setup</code></td>
        <td><p align="justify">Settings of chart (Dictionary with the following keys):</p></td>
        <td>Dictionary</td>
    <tr>
        <td><code>name</code></td>
        <td><p align="justify">Path + name figure (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>width</code></td>
        <td><p align="justify">figure width in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    <tr>
        <td><code>height</code></td>
        <td><p align="justify">figure height in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    <tr>
        <td><code>extension</code></td>
        <td><p align="justify">File extension (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>dots_per_inch</code></td>
        <td><p align="justify">The resolution in dots per inch (key required in plot_setup)</p></td>
        <td>Integer</td>
    <tr>
        <td><code>x_axis_label</code></td>
        <td><p align="justify">x axis label (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>x_axis_size</code></td>
        <td><p align="justify">x axis size (key required in plot_setup)</p></td>
        <td>Integer</td>
    <tr>
        <td><code>y_axis_label</code></td>
        <td><p align="justify">y axis label (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>y_axis_size</code></td>
        <td><p align="justify">y axis size (key required in plot_setup)</p></td>
        <td>Integer</td>
    <tr>
        <td><code>axises_color</code></td>
        <td><p align="justify">Axises color (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>labels_size</code></td>
        <td><p align="justify">Labels size (key required in plot_setup)</p></td>
        <td>Integer</td>
    <tr>
        <td><code>labels_color</code></td>
        <td><p align="justify">Labels color (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>chart_color</code></td>
        <td><p align="justify">Chart color (key required in plot_setup)</p></td>
        <td>String</td>
    <tr>
        <td><code>bins</code></td>
        <td><p align="justify">Range representing the width of a single bar (key required in plot_setup)</p></td>
        <td>Integer</td>
    <tr>
        <td><code>dataset</code></td>
        <td><p align="justify">Dataset</p></td>
        <td>List or array</td>
    </tr>
</table>

Output variables
{: .label .label-yellow }

<table style = "width:100%">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
        <th>Type</th>
      </tr>
    </thead>
    <tr>
        <td><code>None</code></td>
        <td>The function displays the plot on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code> </td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align = "justify">
    <i>
        We use the <code>histogram_chart</code> function to plot a series of random numbers with normal distribution.
    </i>
</p>

```python
# pip install easyplot-toolbox
# or
# pip install --upgrade easyplot-toolbox 
from easyplot_toolbox import *
# or
# from easyplot_toolbox import histogram_chart

# Data
df = np.random.normal(0, 1, 1000)

# Chart config
chart_config = {
              'name': "histogram_chart",
              'width': 16, 
              'height': 8,
              'extension': 'png',
              'dots_per_inch': 600,
              'x_axis_label': '$x_{i}$ variable',
              'x_axis_size': 25,
              'y_axis_label': 'Frequency',
              'y_axis_size': 12,
              'axises_color': 'red',
              'labels_size': 15,
              'labels_color': '#0E6251', 
              'chart_color': '#581845',
              'bins': 20,
             }

# Call function
histogram_chart(dataset=df, plot_setup=chart_config)
```

Example 2
{: .label .label-blue }

<p align = "justify">
    <i>
        We will do the same example shown earlier but using the function inside a looping.
    </i>
</p>

```python
# pip install easyplot-toolbox
# or
# pip install --upgrade easyplot-toolbox 
from easyplot_toolbox import *
# or
# from easyplot_toolbox import histogram_chart

# Data
data = [list(np.random.normal(0, 1, 1000)),
        list(np.random.normal(-5, 2, 1000)),
        list(np.random.normal(10, 1, 1000))]

# Plot in looping
names_and_colors = [['$x_{1}$', '#8C0C15'], 
                    ['$x_{2}$', '#5FD34D'],
                    ['$x_{3}$', '#4DA7D3']]
                    
for i in range(len(names_and_colors)):
    # Chart config
    chart_config = {
                    'name': f"figure_01-{i}_histogram_chart",
                    'extension': 'svg',
                    'width': 16, 
                    'height': 8,
                    'dots_per_inch': 600,
                    'x_axis_label': names_and_colors[i][0],
                    'x_axis_size': 15,
                    'y_axis_label': 'Frequency',
                    'y_axis_size': 15,
                    'axises_color': '#000000',
                    'labels_size': 15,
                    'labels_color': '#000000', 
                    'chart_color': names_and_colors[i][1],
                    'bins': 20,
                    }

    # Call function
    histogram_chart(dataset=data[i], plot_setup=chart_config)
```