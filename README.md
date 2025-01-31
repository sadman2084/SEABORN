# Seaborn

## Introduction
Seaborn is a powerful Python visualization library based on Matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

## Installation
To install Seaborn, use the following command:

```bash
pip install seaborn
```

## Key Features
- Built-in themes for better aesthetics
- Functions for visualizing statistical relationships
- Integration with Pandas data structures
- Automatic estimation and plotting of linear regression models
- Functions for univariate and bivariate distributions
- Capability to handle categorical data effectively

## Basic Usage
```python
import seaborn as sns
import matplotlib.pyplot as plt

# Load example dataset
df = sns.load_dataset("tips")

# Create a simple scatter plot
sns.scatterplot(x="total_bill", y="tip", data=df)
plt.show()
```

## Commonly Used Plots
- **Scatter Plot**: `sns.scatterplot()`
- **Line Plot**: `sns.lineplot()`
- **Bar Plot**: `sns.barplot()`
- **Histogram**: `sns.histplot()`
- **Box Plot**: `sns.boxplot()`
- **Heatmap**: `sns.heatmap()`

## Documentation
For more details, visit the official Seaborn documentation: [Seaborn Docs](https://seaborn.pydata.org/)

