---
layout: home
title: line_chart
parent: Charts
nav_order: 2
has_toc: false
---

<h3>line_chart</h3>

<br>

<p align = "justify">
    This function shows a multiple lines in single chart.
</p>

```python
line_chart(**kwargs)
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
    </tr>
    <tr>
        <td><code>name</code></td>
        <td><p align="justify">Path + name figure (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>width</code></td>
        <td><p align="justify">figure width in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>height</code></td>
        <td><p align="justify">figure height in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>extension</code></td>
        <td><p align="justify">File extension (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>dots_per_inch</code></td>
        <td><p align="justify">The resolution in dots per inch (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>marker</code></td>
        <td><p align="justify">List of markers. See <a href="https://matplotlib.org/stable/gallery/lines_bars_and_markers/marker_reference.html#sphx-glr-gallery-lines-bars-and-markers-marker-reference-py" target="_blank">gallery</a> (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>marker_size</code></td>
        <td><p align="justify">List of marker sizes (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>line_width</code></td>
        <td><p align="justify">List of line widths (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>line_style</code></td>
        <td><p align="justify">List of line styles. See <a href="https://matplotlib.org/stable/gallery/lines_bars_and_markers/linestyles.html" target="_blank">gallery</a> (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>x_axis_label</code></td>
        <td><p align="justify">x axis label (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>x_axis_size</code></td>
        <td><p align="justify">x axis size (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>y_axis_label</code></td>
        <td><p align="justify">y axis label (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>y_axis_size</code></td>
        <td><p align="justify">y axis size (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>axises_color</code></td>
        <td><p align="justify">Axises color (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>labels_size</code></td>
        <td><p align="justify">Labels size (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>labels_color</code></td>
        <td><p align="justify">Labels color (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>chart_color</code></td>
        <td><p align="justify">List of chart_colors (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>x_limit</code></td>
        <td><p align="justify">x axis limits (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>y_limit</code></td>
        <td><p align="justify">y axis limits (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>on_grid</code></td>
        <td><p align="justify">Grid on or off (key required in plot_setup)</p></td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td><code>y_log</code></td>
        <td><p align="justify">y log scale (key required in plot_setup)</p></td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td><code>x_log</code></td>
        <td><p align="justify">x log scale (key required in plot_setup)</p></td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td><code>legend</code></td>
        <td><p align="justify">List of legends (key required in plot_setup)</p></td>
        <td>List</td>
    </tr>
    <tr>
        <td><code>legend_location</code></td>
        <td><p align="justify">Legend location (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>size_legend</code></td>
        <td><p align="justify">Legend size (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>dataset</code></td>
        <td><p align="justify">Dataset with the following</p></td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>x0</code></td>
        <td><p align="justify">x axis values for the first line (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>y0</code></td>
        <td><p align="justify">y axis values for the first line (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>x1</code></td>
        <td><p align="justify">x axis values for the second line (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>y1</code></td>
        <td><p align="justify">y axis values for the second line (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>xn</code></td>
        <td><p align="justify">x axis values for the n-th line (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>yn</code></td>
        <td><p align="justify">y axis values for the n-th line (key required in dataset)</p></td>
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
        We use the <code>line_chart</code> function to plot a series of banana prices.
    </i>
</p>

```python
# Data
df =  {
        'x0': [2012, 2013, 2014, 2015, 2016],
        'y0': [2.50, 3.00, 2.20, 4.50, 3.50]
      }

# Chart setup
chart_config = {
                'name': 'figure_021_line_chart',
                'width': 16.0, 
                'height': 8.0,
                'extension': 'svg',
                'dots_per_inch': 600, 
                'marker': [None],
                'marker_size': [20],
                'line_width': [4],
                'line_style': ['-'],
                'x_axis_label': 'year',
                'x_axis_size': 10,
                'y_axis_label': 'price ($)',
                'y_axis_size': 10,
                'axises_color': 'red',
                'labels_size': 14,
                'labels_color': 'blue',
                'chart_color': ['#000000'],
                'on_grid': True,
                'legend': ['banana'], # or without legend 'legend': [none]
                'legend_location': 'upper left',
                'x_limit': [2012, 2016],
                'y_limit': [2, 5.00],
                'size_legend': 12,
                'y_log': False,
                'x_log': False,
            }

# Call function
line_chart(dataset=df, plot_setup=chart_config)
```

<center>
    <img src="assets/images/line1.svg">
    <p align="center"><b>Figure 1.</b> Line chart</p>
</center>


Example 2
{: .label .label-blue }

<p align = "justify">
    <i>
        We use the <code>line_chart</code> function to plot a series of fruit prices.
    </i>
</p>

```python
# Data statement 
df =  {
        'x0': [2012, 2013, 2014, 2015, 2016],
        'y0': [2.5, 3.0, 2.2, 4.5, 3.5],
        'x1': [2012, 2016],
        'y1': [2.2, 3.2],
        'x2': [2012, 2013, 2014, 2015, 2016],
        'y2': [2.6, 2.9, 2.3, 4.2, 3.6]
       }

# Chart setup
chart_config = {
                'name': 'figure_022_line_chart',
                'width': 16.0, 
                'height': 8.0,
                'extension': 'svg',
                'dots_per_inch': 600, 
                'marker': [None, None, None],
                'marker_size': [3, 3, 3],
                'line_width': [3, 3, 3],
                'line_style': ['--', '-', 'dotted'],
                'x_axis_label': 'Year',
                'x_axis_size': 10,
                'y_axis_label': 'Price ($)',
                'y_axis_size': 10,
                'axises_color': '#000000',
                'labels_size': 14,
                'labels_color': '#000000',
                'chart_color': ['#000000','olive','r'],
                'on_grid': True,
                'legend': ['Banana', 'Apple', 'Orange'],
                'legend_location': 'upper left',
                'size_legend': 8,
                'x_limit': None,
                'y_limit': None,
                'y_log': False,
                'x_log': False,
               }

# Call function
line_chart(dataset=df, plot_setup=chart_config)
```

<center>
    <img src="assets/images/line2.svg">
    <p align="center"><b>Figure 2.</b> Line chart</p>
</center>