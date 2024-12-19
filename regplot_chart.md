---
layout: home
title: regplot_chart
parent: Charts
nav_order: 13
has_toc: false
---

<h3>regplot_chart</h3>

<br>

<p align="justify">
    This function creates a scatter plot with a regression line using seaborn and matplotlib.

</p>

```python
regplot_chart(**kwargs)
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
            <p align="justify">Setup chart Dictionary with the following keys:</p>
            <ul>
                <li><code>name</code>: Path + name of the figure</li>
                <li><code>width</code>: Figure width in SI units</li>
                <li><code>height</code>: Figure height in SI units</li>
                <li><code>marker_size</code>: Size of the scatter plot markers</li>
                <li><code>SCATTER color</code>: Color of the scatter plot markers</li>
                <li><code>line color</code>: Color of the regression line</li>
                <li><code>ORDER</code>: Order of the polynomial regression</li>
                <li><code>y_axis_label</code>: y axis label</li>
                <li><code>y_axis_size</code>: y axis size</li>
                <li><code>x_axis_label</code>: x axis label</li>
                <li><code>x_axis_size</code>: x axis size</li>
                <li><code>labels_size</code>: Labels size</li>
                <li><code>labels_color</code>: Labels color</li>
                <li><code>axises_color</code>: Axes color</li>
                <li><code>on_grid</code>: Grid on or off</li>
                <li><code>y_log</code>: y log scale</li>
                <li><code>x_log</code>: x log scale</li>
                <li><code>dots_per_inch</code>: The resolution in dots per inch</li>
                <li><code>extension</code>: File extension</li>
            </ul>
        </td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>dataset</code></td>
        <td>
            <p align="justify">Dataset.</p>
        </td>
        <td>Dictionary</td>
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
        <td>The function displays the plot on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code> </td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align="justify">
    <i>
        Use the <code>regplot_chart</code> function to create a scatter plot with a regression line.
    </i>
</p>

```python
# Data
HEIGHT = list(np.random.normal(165, 10, 2000))
WEIGHT = list(np.random.logistic(50, 4, 2000))
DF =  pd.DataFrame({'x': HEIGHT,
                    'y': WEIGHT,
                   })
    
# Chart setup
CHART_CONFIG = {
        'name': 'figure1-11-1',
        'width': 10,
        'height': 10,
        'marker size': 25,
        'SCATTER color': 'green',
        'line color': 'red',
        'ORDER': 1,
        'x axis label': 'Weight',
        'x axis size': 15,
        'y axis label': 'Height',
        'y axis size': 15,
        'axises color': 'red',
        'labels size': 15,
        'labels color': 'blue',
        'on grid?': False,
        'y log': False,
        'x log': False,
        'dots per inch': 600,
        'extension': 'svg',
    }


# Data statement 
DATA = {'dataset': DF}

# Call function
regplot_chart(dataset=DATA, plot_setup=CHART_CONFIG)
```

<center><img src="assets/images/regplot_chart.png" width="70%"></center>
<p align="center"><b>Figure 1.</b> Scatter Plot with Regression Line.</p>

[Notebook example](https://drive.google.com/file/d/1rf2oZHfnTU4MBpZyqr25tsnUi26uwgd3/view?usp=sharing){: .btn .btn-outline }

