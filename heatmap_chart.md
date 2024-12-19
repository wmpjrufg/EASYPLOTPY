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
        <td>
            <p align="justify">Setup chart Dictionary with the following keys:</p>
            <ul>
                <li><code>name</code>: Path + name of the figure</li>
                <li><code>width</code>: Figure width in SI units</li>
                <li><code>height</code>: Figure height in SI units</li>
                <li><code>extension</code>: File extension</li>
                <li><code>dots_per_inch</code>: The resolution in dots per inch</li>
                <li><code>mask</code>: Whether to use a mask for the upper triangle</li>
                <li><code>line_widths</code>: Width of the lines between cells</li>
                <li><code>color map</code>: Color map for the heatmap</li>
                <li><code>line color</code>: Color of the lines between cells</li>
                <li><code>annot</code>: Whether to annotate each cell with the correlation value</li>
                <li><code>annot size font</code>: Font size of the annotations</li>
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
        <td>The function displays the heatmap on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code></td>
        <td>None</td>
    </tr>
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
