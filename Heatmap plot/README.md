# **Seaborn Heatmap Visualization**

## **Overview**  
This script uses **Seaborn's heatmap** to visualize numerical data from the **car_crashes** dataset. It also demonstrates various customizations like **color maps, annotations, grid lines, and axis labels**.  

---

## **Requirements**  
Ensure you have the necessary libraries installed before running the script:  

```bash
pip install matplotlib seaborn pandas numpy
```

---

## **Code Explanation**  

### **1. Importing Required Libraries**  

```python
import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
import numpy as np
```
- `matplotlib.pyplot` → For plotting  
- `pandas` → For handling datasets  
- `seaborn` → For advanced visualizations  
- `numpy` → For numerical operations  

---

### **2. Loading the Dataset**  

```python
data_load = sns.load_dataset("car_crashes")
```
- Loads the **car_crashes** dataset, which contains U.S. state-wise car crash statistics.  

---

### **3. Creating a NumPy Array**  

```python
var = np.linspace(1, 10, 20).reshape(4, 5)
```
- **`linspace(1, 10, 20)`** → Generates **20** evenly spaced numbers between **1 and 10**.  
- **`reshape(4, 5)`** → Reshapes the array into **4 rows and 5 columns**.  

---

### **4. Preparing Data for Heatmap**  

```python
x = data_load.drop(columns=["abbrev"], axis=1).head(20)
```
- Removes the **"abbrev"** column (which contains state abbreviations) since **heatmaps only work with numerical data**.  
- **`head(20)`** → Selects the first **20 rows**.  

---

### **5. Basic Heatmap Visualization**  

```python
sns.heatmap(x, vmin=0, vmax=20, cmap="PuOr", annot=True)
```
- **`vmin=0, vmax=20`** → Limits the color range from **0 to 20**.  
- **`cmap="PuOr"`** → Uses the **"PuOr" (Purple-Orange) color palette**.  
- **`annot=True`** → Displays **numeric values inside each cell**.  

---

### **6. Heatmap with Custom Annotations**  

```python
var = np.linspace(1, 10, 10).reshape(2, 5)

ar = np.array([["a0", "a1", "a2", "a3", "a4"], ["b0", "b1", "b2", "b3", "b4"]])
sns.heatmap(var, vmin=0, vmax=20, cmap="PuOr", annot=ar, fmt="s")
```
- **`annot=ar`** → Uses **custom text labels** inside each heatmap cell.  
- **`fmt="s"`** → Ensures text formatting is correctly applied.  

---

### **7. Advanced Heatmap with Customizations**  

```python
y = {"fontsize": 10, "color": "green"}
v = sns.heatmap(
    x, vmin=0, vmax=20, cmap="PuOr", annot=True, annot_kws=y, linewidth=4,
    linecolor="yellow", cbar=False, xticklabels=False
)
v.set(xlabel="python", ylabel="nothing")
sns.set(font_scale=1)
```
#### **Customizations:**
- **`annot_kws=y`** → Custom annotation style (**green text, font size 10**).  
- **`linewidth=4`** → **Thicker grid lines (4 px)** between heatmap cells.  
- **`linecolor="yellow"`** → **Yellow grid lines**.  
- **`cbar=False`** → Removes the **color bar**.  
- **`xticklabels=False`** → **Hides x-axis labels**.  
- **`set(xlabel="python", ylabel="nothing")`** → Changes **axis labels**.  
- **`sns.set(font_scale=1)`** → Adjusts **font size** for the entire plot.  

---

### **8. Displaying the Plot**  

```python
plt.show()
```
- **Displays the final heatmap visualization.**  

---

## **Output Example**  
The script will generate multiple **heatmaps** with different styles, including:  
✅ **Basic heatmap with annotations**  
✅ **Heatmap with custom text labels**  
✅ **Advanced heatmap with grid lines, colors, and labels**  

---

## **Conclusion**  
This script demonstrates how to **customize Seaborn heatmaps** using:  
- **Color palettes (`cmap`)**  
- **Annotations (`annot`, `annot_kws`)**  
- **Grid styles (`linewidth`, `linecolor`)**  
- **Axis customizations (`xlabel`, `ylabel`, `xticklabels`)**  

Seaborn heatmaps are useful for **visualizing correlations, statistics, and numerical relationships** in datasets.  

---

Let me know if you need further improvements! 🚀
