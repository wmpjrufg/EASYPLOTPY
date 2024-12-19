---
layout: home  
title: heatmap_chart  
parent: Charts  
nav_order: 5  
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

<h3>Input Variables</h3>
{: .label .label-yellow }

<table style="width:100%;">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Type</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>plot_setup</code></td>
            <td>
                <p align="justify">Dictionary for heatmap configuration, including the following keys:</p>
                <ul>
                    <li><code>name</code>: Path and name of the output figure file</li>
                    <li><code>width</code>: Width of the figure (in SI units)</li>
                    <li><code>height</code>: Height of the figure (in SI units)</li>
                    <li><code>extension</code>: File extension for the saved figure</li>
                    <li><code>dots_per_inch</code>: Resolution of the figure in dots per inch (DPI)</li>
                    <li><code>mask</code>: Boolean indicating whether to mask the upper triangle of the heatmap</li>
                    <li><code>line_widths</code>: Width of the lines between cells in the heatmap</li>
                    <li><code>color_map</code>: Colormap to use for the heatmap</li>
                    <li><code>line_color</code>: Color of the grid lines between cells</li>
                    <li><code>annot</code>: Boolean indicating whether to annotate cells with correlation values</li>
                    <li><code>annot_font_size</code>: Font size for the annotations</li>
                </ul>
            </td>
            <td>Dictionary</td>
        </tr>
        <tr>
            <td><code>dataset</code></td>
            <td>
                <p align="justify">Array-like dataset containing the values for plotting the heatmap</p>
            </td>
            <td>List or array</td>
        </tr>
    </tbody>
</table>

<h3>Output Variables</h3>
{: .label .label-yellow }

<table style="width:100%;">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Type</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>None</code></td>
            <td>
                <p align="justify">The function displays the heatmap on the screen and saves it to the local folder of the script or notebook (<code>.ipynb</code> or <code>.py</code>).</p>
            </td>
            <td>None</td>
        </tr>
    </tbody>
</table>


Example 1  
{: .label .label-blue }

<p align = "justify">
    <i>
        Use the <code>heatmap_chart</code> function to generate a heatmap.
    </i>
</p>

```python
# Data
DF = pd.DataFrame({ 'A1': [random.randint(1, 100) for _ in range(10)],
                    'A2': [random.randint(1, 100) for _ in range(10)],
                    'A3': [random.randint(1, 100) for _ in range(10)],
                    'A4': [random.randint(1, 100) for _ in range(10)],
                    'A5': [random.randint(1, 100) for _ in range(10)]
                  })

# Chart setup
plot_setup = {
    'name': 'figure1-7-1',
    'width': 30,
    'height': 15,
    'mask': False,
    'line widths': 8,
    'color map': 'plasma',
    'line color': 'white',
    'annot': True,
    'annot size font': 12,
    'dots per inch': 600,
    'extension': 'svg'
}


# Data statement 
DATA = {'dataset': DF}

# Call function
heatmap_chart(dataset = DATA, plot_setup = plot_setup)
```

<center><img src="assets/images/heatmap-figure.png" width="70%"></center>
<p align = "center"><b>Figure 1.</b> Heatmap of DataFrame Correlation.</p> 
