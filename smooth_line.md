---
layout: home
title: smooth_line
parent: Charts
nav_order: 8
has_toc: false
---

<h3>smooth_line</h3>

<br>

<p align="justify">
    This function creates a smooth line chart with optional log scales, grid, and customization options for line styles, colors, and labels.

</p>

```python
smooth_line(**kwargs)
```

Input variables
{: .label .label-yellow }

<table style="width:100%">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
        <th>Type</th>
      </tr>
    </thead>
    <tr>
        <td><code>plot_setup</code></td>
        <td>
            <p align="justify">Setup chart dictionary with the following keys:</p>
            <ul>
                <li><code>name</code>: Path + name of the figure</li>
                <li><code>width</code>: Figure width in SI units</li>
                <li><code>height</code>: Figure height in SI units</li>
                <li><code>extension</code>: File extension</li>
                <li><code>dots_per_inch</code>: Resolution in dots per inch</li>
                <li><code>line_width</code>: List of line widths</li>
                <li><code>line_style</code>: List of line styles</li>
                <li><code>y_axis_label</code>: y axis label</li>
                <li><code>x_axis_label</code>: x axis label</li>
                <li><code>labels_size</code>: Labels size</li>
                <li><code>labels_color</code>: Labels color</li>
                <li><code>x_axis_size</code>: x axis size</li>
                <li><code>y_axis_size</code>: y axis size</li>
                <li><code>axises_color</code>: Axes color</li>
                <li><code>x_limit</code>: x axis limits</li>
                <li><code>y_limit</code>: y axis limits</li>
                <li><code>chart_color</code>: List of chart colors</li>
                <li><code>on_grid</code>: Grid on or off</li>
                <li><code>y_log</code>: y log scale</li>
                <li><code>x_log</code>: x log scale</li>
                <li><code>legend_location</code>: Legend location</li>
                <li><code>size_legend</code>: Legend size</li>
            </ul>
        </td>
        <td>Dictionary</td>
    </tr>
        <tr>
            <td><code>dataset</code></td>
            <td>
                <p align="justify">Dataset to plot</p>
            </td>
            <td>List or array</td>
        </tr>
    </tbody>    
</table>

Output variables
{: .label .label-yellow }

<table style="width:100%">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
        <th>Type</th>
      </tr>
    </thead>
    <tr>
        <td><code>None</code></td>
        <td>The function displays the smooth line chart on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code></td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align="justify">
    <i>
        Use the <code>smooth_line</code> function to create a smooth line chart from the dataset.
    </i>
</p>

```python
from easyplot_toolbox.easyplot import smooth_line
import numpy as np

x = np.linspace(0, 10, 100)
curve1 = np.sin(x) + np.random.normal(0, 0.1, len(x))
curve2 = np.sin(x) + np.random.normal(0, 0.1, len(x))
curve3 = np.sin(x) + np.random.normal(0, 0.1, len(x))

df = {
    'x': x,
    'curve1': curve1,
    'curve2': curve2,
    'curve3': curve3
}

# Chart setup
chart_config = {
    'name': 'smooth_line_with_confidence_interval',
    'width': 20,  
    'height': 15, 
    'extension': 'jpg',
    'dots_per_inch': 100,
    'line_width': [2],  
    'line_style': ['-'],  
    'y_axis_label': 'Axis Y',
    'x_axis_label': 'Axis X',
    'labels_size': 12,
    'labels_color': 'black',
    'x_axis_size': 10,
    'y_axis_size': 10,
    'axises_color': 'gray',
    'x_limit': [0, 10],  
    'y_limit': [None, None],  
    'chart_color': ['blue'],  
    'on_grid': True,
    'y_log': False,
    'x_log': False,
    'legend_location': 'best',
    'size_legend': 10,
}

# Call function
smooth_line(dataset=df, plot_setup=chart_config)
```

<center><img src="assets/images/smooth_line_with_confidence_interval.jpg" width="70%"></center>
<p align="center"><b>Figure 1.</b> Joyplot of the dataset.</p>

[Notebook example](https://drive.google.com/file/d/1rf2oZHfnTU4MBpZyqr25tsnUi26uwgd3/view?usp=sharing){: .btn .btn-outline }