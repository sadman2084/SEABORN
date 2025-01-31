# Seaborn Pair Plots with Custom Styling

## Overview
This Python script utilizes the `seaborn` and `matplotlib` libraries to create various pair plots based on the "tips" dataset. The script demonstrates multiple ways to visualize relationships between different numerical columns using pair plots with customizations like hue, variables selection, density lines, and marker styles.

## Prerequisites
Before running the script, ensure you have the required libraries installed. You can install them using:

```bash
pip install matplotlib seaborn pandas
```

## Code Explanation

### Importing Libraries
```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
```
- `matplotlib.pyplot` is used for plotting functionalities.
- `seaborn` provides high-level visualization tools.
- `pandas` is included for dataset manipulation.

### Loading the Dataset
```python
data_load = sns.load_dataset("tips").head(20)
```
- Loads the built-in "tips" dataset, which contains details about restaurant bills, including total bill, tip amount, gender, and day of the week.
- `head(20)`: Selects the first 20 rows for visualization.

### Creating a Basic Pair Plot with Hue for Gender
```python
sns.pairplot(data_load, hue="sex")
plt.show()
```
- `sns.pairplot()` creates scatter plots for all numerical columns against each other.
- `hue="sex"`: Differentiates the data points by gender (Male/Female).

### Creating a Pair Plot for Specific Columns
```python
sns.pairplot(data_load, vars=["total_bill", "tip"], hue="sex", hue_order=["Female", "Male"], palette="Accent")
plt.show()
```
- `vars=["total_bill", "tip"]`: Limits the pair plot to only the `total_bill` and `tip` columns.
- `hue="sex"`: Colors the points based on gender.
- `hue_order=["Female", "Male"]`: Displays Female first and then Male.
- `palette="Accent"`: Uses the "Accent" color palette.

### Creating a Pair Plot with X-Axis Selection
```python
sns.pairplot(data_load, x_vars=["total_bill", "tip"])
plt.show()
```
- `x_vars=["total_bill", "tip"]`: Only shows plots with these columns on the x-axis.

### Creating a Pair Plot with Y-Axis Selection
```python
sns.pairplot(data_load, y_vars=["total_bill", "tip"])
plt.show()
```
- `y_vars=["total_bill", "tip"]`: Only shows plots with these columns on the y-axis.

### Creating a Pair Plot with Density Lines
```python
sns.pairplot(data_load, kind="reg", diag_kind="kde")
plt.show()
```
- `kind="reg"`: Adds regression lines to scatter plots.
- `diag_kind="kde"`: Uses kernel density estimation (KDE) for diagonal plots instead of histograms.
- Other `kind` options: "scatter", "kde", "hist", "reg".
- Other `diag_kind` options: "scatter", "kde", "hist", "reg".

### Changing the Marker Style in Pair Plots
```python
sns.pairplot(data_load, markers=["*", "<"])
plt.show()
```
- `markers=["*", "<"]`: Uses `*` for one category and `<` for another.
- Helps differentiate data points more clearly.

## Expected Output
The script generates multiple pair plots showcasing the relationships between numerical columns, with customizations such as hue distinctions, selected variables, density plots, regression lines, and different markers.

## Customization Options
- Modify `vars` to include other numerical columns.
- Adjust `hue` to group data by a different categorical variable (e.g., `day`).
- Experiment with `kind` and `diag_kind` for different visualization styles.
- Change `palette` to different color schemes like `Blues`, `coolwarm`, or `viridis`.
- Customize `markers` for different categorical values.

