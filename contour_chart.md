---
layout: home
title: contour_chart
parent: Charts
nav_order: 6
has_toc: false
---

<h3>contour_chart</h3>

<br>

<p align="justify">
    This function creates a filled contour plot using matplotlib.

</p>

```python
contour_chart(dataset, plot_setup)
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
        <td><code>X</code></td>
        <td><p align="justify">Array-like object of x-coordinates (key required in dataset)</p></td>
        <td>Array-like</td>
    </tr>
    <tr>
        <td><code>Y</code></td>
        <td><p align="justify">Array-like object of y-coordinates (key required in dataset)</p></td>
        <td>Array-like</td>
    </tr>
    <tr>
        <td><code>Z</code></td>
        <td><p align="justify">Array-like object of z-values (key required in dataset)</p></td>
        <td>Array-like</td>
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
        <td><code>dots_per_inch</code></td>
        <td><p align="justify">Resolution in dots per inch (key required in plot_setup)</p></td>
        <td>Integer</td>
    </tr>
    <tr>
        <td><code>extension</code></td>
        <td><p align="justify">File extension (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>TITLE</code></td>
        <td><p align="justify">Title for the color bar (key required in plot_setup)</p></td>
        <td>String</td>
    </tr>
    <tr>
        <td><code>LEVELS</code></td>
        <td><p align="justify">Levels for the contour plot (key required in plot_setup)</p></td>
        <td>Array-like</td>
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
        <td>The function displays the contour plot on the screen and saves it to the local folder of the <code>.ipynb</code> or <code>.py</code></td>
        <td>None</td>
    </tr>
</table>

Example 1
{: .label .label-blue }

<p align="justify">
    <i>
        Use the <code>contour_chart</code> function to create a filled contour plot.
    </i>
</p>

```python
# Data
X, Y = np.meshgrid(np.linspace(-5, 10, 100),
                   np.linspace(-5, 10, 100))
Z = np.sqrt(X ** 2 + Y ** 2)

setup = {
    'NAME': 'CONTOUR',         
    'DPI': 600, 
    'EXTENSION': 'svg',
    'TITLE': 'Color bar title',
    'LEVELS': 25
}
dataset = {
    'X': X,
    'Y': Y,
    'Z': Z
}
contour_chart(DATASET=dataset, PLOT_SETUP=setup)
```

<center><img src="assets/images/contour_plot.png" width="70%"></center>
<p align="center"><b>Figure 1.</b> Filled Contour Plot.</p>

[Notebook example](https://drive.google.com/file/d/1rf2oZHfnTU4MBpZyqr25tsnUi26uwgd3/view?usp=sharing){: .btn .btn-outline }
