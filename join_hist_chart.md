---
layout: home
title: join_hist_chart
parent: Charts
nav_order: 7
has_toc: false
---

<h3>join_hist_chart</h3>

<br>

<p align="justify">
    This function creates a joyplot (also known as a stacked density plot) using matplotlib and joypy.

</p>

```python
join_hist_chart(**kwargs)
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
        <td><code>dataset</code></td>
        <td><p align="justify">Dictionary containing the data to plot. Must include:</p></td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>dataset['dataset']</code></td>
        <td><p align="justify">DataFrame with the data to be plotted.</p></td>
        <td>DataFrame</td>
    </tr>
    <tr>
        <td><code>plot_setup</code></td>
        <td><p align="justify">Setup chart Dictionary with the following keys:</p></td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>name</code></td>
        <td><p align="justify">Path + name of the figure (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>width</code></td>
        <td><p align="justify">Width of the plot (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>height</code></td>
        <td><p align="justify">Height of the plot (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>x_axis_size</code></td>
        <td><p align="justify">Font size for the x-axis labels (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>X axIS color</code></td>
        <td><p align="justify">Color of the x-axis and y-axis labels (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>dots_per_inch</code></td>
        <td><p align="justify">Resolution in dots per inch (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>extension</code></td>
        <td><p align="justify">File extension (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
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
        <td>The function displays the joyplot on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code></td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align="justify">
    <i>
        Use the <code>join_hist_chart</code> function to create a joyplot of the dataset.
    </i>
</p>

```python
# Data
import pandas as pd
import numpy as np

# Generating sample data
np.random.seed(0)
data = pd.DataFrame({
    'A': np.random.normal(loc=0, scale=1, size=100),
    'B': np.random.normal(loc=1, scale=2, size=100),
    'C': np.random.normal(loc=2, scale=3, size=100),
})

# Chart setup
chart_config = {
    'name': 'joyplot',
    'width': 10,
    'height': 6,
    'x_axis_size': 12,
    'X axIS color': 'black',
    'dots_per_inch': 300,
    'extension': 'png',
}

# Call function
join_hist_chart(dataset={'dataset': data}, plot_setup=chart_config)
```

<center><img src="assets/images/joyplot.png" width="70%"></center>
<p align="center"><b>Figure 1.</b> Joyplot of the dataset.</p>

[Notebook example](https://drive.google.com/file/d/1rf2oZHfnTU4MBpZyqr25tsnUi26uwgd3/view?usp=sharing){: .btn .btn-outline }