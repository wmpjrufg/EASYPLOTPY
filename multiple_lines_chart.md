---
layout: home
title: multiple_lines_chart
parent: Charts
nav_order: 7
has_toc: false
---

<h3>multiple_lines_chart</h3>

<br>

<p align = "justify">
    This function creates a line chart with two y-axes, allowing for the display of multiple lines with different scales on the same chart.
</p>

```python
multiple_lines_chart(**kwargs)
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
        <td><code>marker</code></td>
        <td><p align="justify">Markers for the lines (key required in plot_setup)</p></td>
        <td>List of Strings</td>
    </tr>
    <tr>
        <td><code>marker_size</code></td>
        <td><p align="justify">Size of the markers (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>line_width</code></td>
        <td><p align="justify">Width of the lines (key required in plot_setup)</p></td>
        <td>Float</td>
    </tr>
    <tr>
        <td><code>line_style</code></td>
        <td><p align="justify">Line styles (key required in plot_setup)</p></td>
        <td>List of Strings</td>
    </tr>
    <tr>
        <td><code>Y0_axIS_LABEL</code></td>
        <td><p align="justify">Label for the primary y-axis (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>Y1_axIS_LABEL</code></td>
        <td><p align="justify">Label for the secondary y-axis (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>x_axis_label</code></td>
        <td><p align="justify">Label for the x-axis (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>labels_size</code></td>
        <td><p align="justify">Size of the labels (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>x_axis_size</code></td>
        <td><p align="justify">Size of the x-axis labels (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>y_axis_size</code></td>
        <td><p align="justify">Size of the y-axis labels (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>chart_color</code></td>
        <td><p align="justify">List of colors for the lines (key required in plot_setup)</p></td>
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
        <td><p align="justify">Legend labels (key required in plot_setup)</p></td>
        <td>List of Strings</td>
    </tr>
    <tr>
        <td><code>legend_location</code></td>
        <td><p align="justify">Location of the legend (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>size_legend</code></td>
        <td><p align="justify">Font size of the legend (key required in plot_setup)</p></td>
        <td>Integer</td>
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
        <td>The function displays the plot on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code></td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align = "justify">
    <i>
        Use the <code>multiple_lines_chart</code> function to visualize multiple lines with two y-axes.
    </i>
</p>

```python
# Data
X = np.arange(0.01, 10.0, 0.01)
DATA_1 = np.exp(X)
DATA_2 = X * np.sin(2 * np.pi * X + 2)
DF =  pd.DataFrame({
                    'x': list(X),
                    'y0': list(DATA_1),
                    'y1': list(DATA_2)
                   })

# Chart setup
CHART_CONFIG = {
              'NAME': 'figure1-10-1',
              'WIDTH': 20., 
              'HEIGHT': 10,
              'MARKER': ['none', 'none'],
              'MARKER SIZE': 2,
              'LINE WIDTH': 2,
              'LINE STYLE': ['-', '-'],
              'X AXIS LABEL': 'time ($s$)',
              'X AXIS SIZE': 12,
              'Y0 AXIS LABEL': 'rpm ($rot \cdot min^{-1}$)',
              'Y1 AXIS LABEL': 'vibration signal ($mm$)',
              'Y AXIS SIZE': 12,
              'LABELS SIZE': 14,
              'CHART COLOR': ['red', 'blue'],
              'ON GRID?': True,
              'LEGEND': ['motor speed', 'vibration signal'],
              'LOC LEGEND': 'upper left',
              'SIZE LEGEND': 12,
              'Y LOG': False,
              'X LOG': False,
              'DPI': 600, 
              'EXTENSION': 'svg'
             }

# Data statement 
DATA = {'DATASET': DF}

# Call function
multiple_lines_chart(DATASET = DATA, PLOT_SETUP = CHART_CONFIG)
```

<center><img src="assets/images/multiples_lines.png" width="70%"></center>
<p align = "center"><b>Figure 2.</b> Data Visualization with Two Y-Axes.</p>
```