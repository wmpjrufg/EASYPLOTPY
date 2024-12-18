---
layout: default
title: heatmap_chart
grand_parent: Framework
parent: Common Library functions
nav_order: 10
has_toc: false
---

<h3>heatmap_chart</h3>

<br>

<p align = "justify">
    This function creates a heatmap chart.


</p>

```python
heatmap_chart(**kwargs)
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
        <td><p align="justify">Setup chart dictionary with the following keys:</p></td>
        <td>dictionary</td>
    </tr>
    <tr>
        <td><code>name</code></td>
        <td><p align="justify">Path + name figure (key required in plot_setup)</p></td>
        <td>string</td>
    </tr>
    <tr>
        <td><code>width</code></td>
        <td><p align="justify">Figure width in SI units (key required in plot_setup)</p></td>
        <td>float</td>
    </tr>
    <tr>
        <td><code>height</code></td>
        <td><p align="justify">Figure height in SI units (key required in plot_setup)</p></td>
        <td>float</td>
    </tr>
    <tr>
        <td><code>extension</code></td>
        <td><p align="justify">File extension (key required in plot_setup)</p></td>
        <td>string</td>
    </tr>
    <tr>
        <td><code>dots_per_inch</code></td>
        <td><p align="justify">The resolution in dots per inch (key required in plot_setup)</p></td>
        <td>integer</td>
    </tr>
    <tr>
        <td><code>mask</code></td>
        <td><p align="justify">Whether to use a mask for the upper triangle (key required in plot_setup)</p></td>
        <td>boolean</td>
    </tr>
    <tr>
        <td><code>line_widths</code></td>
        <td><p align="justify">Width of the lines between cells (key required in plot_setup)</p></td>
        <td>float</td>
    </tr>
    <tr>
        <td><code>annot</code></td>
        <td><p align="justify">Whether to annotate each cell with the correlation value (key required in plot_setup)</p></td>
        <td>boolean</td>
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
        Use the <code>heatmap_chart</code> function to perform a task.
    </i>
</p>

```python
# Example code goes here
```

```bash
# Example output goes here
```

