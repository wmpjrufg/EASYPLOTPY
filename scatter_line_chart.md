---
layout: home
title: scatter_line_chart
parent: Charts
nav_order: 4
has_toc: false
---

<h3>scatter_chart</h3>

<br>

<p align = "justify">
    This function shows a scatter chart.


</p>

```python
scatter_line_chart(**kwargs)
```

<!-- Input variables
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
        <td><p align="justify">Setup chart Dictionary with the following keys:</p></td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>name</code></td>
        <td><p align="justify">Path + name figure (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>width</code></td>
        <td><p align="justify">Figure width in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>height</code></td>
        <td><p align="justify">Figure height in SI units (key required in plot_setup)</p></td>
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
        <td><code>marker_size</code></td>
        <td><p align="justify">List of marker sizes (key required in plot_setup)</p></td>
        <td>List</td>
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
        <td><code>axises_color</code></td>
        <td><p align="justify">Axises color (key required in plot_setup)</p></td>
        <td>String</td>
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
        <td><p align="justify">Dataset. Add key 'colorbar' for colorbar in scatterplot</p></td>
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
    <tr>
        <td><code>colorbar</code></td>
        <td><p align="justify">List of colorbar values (key required in dataset when colorbar is used. If not, it is not necessary)</p></td>
        <td>List</td>
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
</table> -->

Example 1
{: .label .label-blue }

<p align = "justify"><i>
We use the <code>scatter_line_chart</code> function to plot a dataset values and your predict values.
</i></p>

```python
# Data
x = np.linspace(0, 10, 20)
y0 = 2 * x + 1 + np.random.normal(0, 1, 20)
y1 = 3 * x + 1.5 + np.random.normal(0, 1, 20)
y3 = 2.5 * x

df_sc =  {
        'x0': list(x),
        'y0': list(y0),
        'x1': list(x),
        'y1': list(y1)
      }

df_li = { 
        'x0': list(x),
        'y0': list(y3)
     }


# Chart setup
setup = {
        'name': 'scatter plot',
        'width': 10, 
        'height': 6,
        'dots_per_inch': 600, 
        'extension': 'svg',
        'marker_line': [None],
        'marker_size_line': [None],
        'marker_size_scatter': [None]*2,
        'line_width': [1.5],
        'line_style': ['-'],
        'y_axis_label': 'Height',
        'x_axis_label': 'Weight',
        'labels_size': 14,
        'labels_color': 'black', 
        'y_axis_size': 14,
        'x_axis_size': 14,
        'axises_color': '#000000',
        'x_limit': None,
        'y_limit': None,
        'chart_color_line': ['blue'],
        'color_map': ['green', 'red'],
        'on_grid': False,
        'y_log': False,
        'x_log': False,
        'legend_line': ['mean value'],
        'legend_scatter': [None]*2,
        'legend_location': 'upper left',
        'size_legend': 12
    }

# Call function
scatter_line_chart(plot_setup=setup, dataset_line=df_li, dataset_sc=df_sc)
```
