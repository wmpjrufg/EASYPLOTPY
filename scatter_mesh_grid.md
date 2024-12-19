---
layout: home
title: scatter_mesh_grid
parent: Charts
nav_order: 12
has_toc: false
---

<h3>scatter_mesh_grid</h3>

<br>

<p align="justify">
    This function creates a scatter mesh grid chart with filled contours and overlayed scatter points.

</p>

```python
scatter_mesh_grid(**kwargs)
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
        <td><p align="justify">Figure width in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>height</code></td>
        <td><p align="justify">Figure height in SI units (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>marker_size</code></td>
        <td><p align="justify">Size of the scatter markers (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>color_map</code></td>
        <td><p align="justify">Color map for the mesh grid (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>y_axis_label</code></td>
        <td><p align="justify">Label for the y axis (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>y_axis_size</code></td>
        <td><p align="justify">Font size for the y axis label (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>x_axis_label</code></td>
        <td><p align="justify">Label for the x axis (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>x_axis_size</code></td>
        <td><p align="justify">Font size for the x axis label (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>labels_size</code></td>
        <td><p align="justify">Font size for labels (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>labels_color</code></td>
        <td><p align="justify">Color of the labels (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>axises_color</code></td>
        <td><p align="justify">Color of the axes (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>on_grid</code></td>
        <td><p align="justify">Whether to display grid lines (key required in plot_setup)</p></td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td><code>y_log</code></td>
        <td><p align="justify">Whether to use a logarithmic scale for the y axis (key required in plot_setup)</p></td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td><code>x_log</code></td>
        <td><p align="justify">Whether to use a logarithmic scale for the x axis (key required in plot_setup)</p></td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td><code>dots_per_inch</code></td>
        <td><p align="justify">Resolution in dots per inch (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>extension</code></td>
        <td><p align="justify">File extension for saving the figure (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>dataset</code></td>
        <td><p align="justify">Dataset with the following keys:</p></td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>x</code></td>
        <td><p align="justify">x axis values (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>y</code></td>
        <td><p align="justify">y axis values (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>z</code></td>
        <td><p align="justify">z axis values (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>x_points</code></td>
        <td><p align="justify">x axis values for the scatter points (key required in dataset)</p></td>
        <td>List or array</td>
    </tr>
    <tr>
        <td><code>y_points</code></td>
        <td><p align="justify">y axis values for the scatter points (key required in dataset)</p></td>
        <td>List or array</td>
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
        <td>The function displays the scatter mesh grid plot on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code></td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align="justify">
    <i>
        Use the <code>scatter_mesh_grid</code> function to create a scatter mesh grid plot with filled contours and scatter points overlayed.
    </i>
</p>

```python
import numpy as np

x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
z = np.sin(np.sqrt(np.add.outer(x**2, y**2))) # Exemplo de função para o mesh grid

# Data
df = {
    'x': y,
    'y': x,
    'z': z,  
    'x_points': np.random.uniform(-5, 5, 100),
    'y_points': np.random.uniform(-5, 5, 100),
}

# Chart setup
chart_config = {
                'name': 'scatter_mesh_grid_plot',
                'width': 8,
                'height': 6,
                'extension': 'jpg',
                'dots_per_inch': 100,
                'marker_size': 10,
                'color_map': 'viridis',
                'y_axis_label': 'Axis Y',
                'y_axis_size': 12,
                'x_axis_label': 'Axis X',
                'x_axis_size': 12,
                'labels_size': 10,
                'labels_color': 'black',
                'axises_color': 'gray',
                'on_grid': True,
                'y_log': False,
                'x_log': False,
            }

# Call function
scatter_mesh_grid(dataset=df, plot_setup=chart_config)
```

<center><img src="assets/images/scatter_mesh_grid_plot.jpg" width="70%"></center>
<p align="center"><b>Figure 1.</b> Scatter Mesh Grid Plot with Filled Contours and Scatter Points.</p>

[Notebook example](https://drive.google.com/file/d/1rf2oZHfnTU4MBpZyqr25tsnUi26uwgd3/view?usp=sharing){: .btn .btn-outline }