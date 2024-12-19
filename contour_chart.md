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

<h3>Input variables</h3>
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
        <td>
            <p align="justify">Dictionary containing the data to plot. Must include:</p>
            <ul>
                <li><code>X</code>: Array-like object of x-coordinates</li>
                <li><code>Y</code>: Array-like object of y-coordinates</li>
                <li><code>Z</code>: Array-like object of z-values</li>
            </ul>
        </td>
        <td>Dictionary</td>
    </tr>
    <tr>
        <td><code>plot_setup</code></td>
        <td>
            <p align="justify">Setup chart Dictionary with the following keys:</p>
            <ul>
                <li><code>name</code>: Path + name of the figure</li>
                <li><code>dots_per_inch</code>: Resolution in dots per inch</li>
                <li><code>extension</code>: File extension</li>
                <li><code>TITLE</code>: Title for the color bar</li>
                <li><code>LEVELS</code>: Levels for the contour plot</li>
            </ul>
        </td>
        <td>Dictionary</td>
    </tr>
</table>

<h3>Output variables</h3>
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
