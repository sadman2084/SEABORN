## Introduction
This script demonstrates how to create a count plot using Seaborn, which visualizes the frequency distribution of categorical variables.

## Prerequisites
Ensure you have the following Python libraries installed before running the script:

```bash
pip install matplotlib pandas seaborn
```

## Code Explanation

### Importing Required Libraries
```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
```
This imports Matplotlib for plotting, Pandas for handling data, and Seaborn for advanced visualizations.

### Loading Dataset
```python
data_load = sns.load_dataset("tips")
```
Loads the built-in "tips" dataset provided by Seaborn, which contains information about restaurant bills, including gender, smoking status, and tips.

### Creating the Count Plot
```python
sns.countplot(x="sex", data=data_load, hue="smoker", color="red", saturation=0.4)
```
This command generates a count plot with various customizations:
- `x="sex"`: The categorical variable "sex" is displayed on the x-axis.
- `data=data_load`: Uses the "tips" dataset.
- `hue="smoker"`: Differentiates the data by smoker status using different colors.
- `color="red"`: Sets the primary color of the bars.
- `saturation=0.4`: Adjusts the intensity of the bar color.

### Additional Notes:
- The count plot shows the count (frequency) of each category.
- Unlike a bar plot, the count plot does not require an explicit y-variable, as it automatically counts occurrences.
- To make the plot vertical, replace `x="sex"` with `y="sex"`.

### Displaying the Plot
```python
plt.show()
```
Renders the count plot on the screen.

## Summary
This script uses Seaborn to create a count plot that visualizes the frequency of male and female customers, with an additional distinction based on smoking status.

## Notes
- The dataset "tips" must be available within Seaborn.
- Ensure that all required libraries are installed and imported properly.

For more details, visit the [Seaborn Documentation](https://seaborn.pydata.org/).

