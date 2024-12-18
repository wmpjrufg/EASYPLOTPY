---
layout: default
title: scatter_line_chart
grand_parent: Framework
parent: Common Library functions
nav_order: 15
has_toc: false
---

<h3>scatter_line_chart</h3>

<br>

<p align = "justify">
    This function shows a multiple lines and scatter points in single chart.


</p>

```python
scatter_line_chart(**kwargs)
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
        <td><code>dataset_line</code></td>
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
    <tr>
        <td><code>dataset_sc</code></td>
        <td><p align="justify">Dataset with the following</p></td>
        <td>Dictionary</td>
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
        Use the <code>scatter_line_chart</code> function to perform a task.
    </i>
</p>

```python
# Example code goes here
```

```bash
# Example output goes here
```

