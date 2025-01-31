## **Overview**  
This script uses **Seaborn's FacetGrid** to create **multiple scatter plots** from the **tips dataset**. It **separates plots by day** and differentiates **genders** using colors.  

---

## **Requirements**  
Ensure you have the necessary libraries installed before running the script:  

```bash
pip install matplotlib seaborn pandas
```

---

## **Code Explanation**  

### **1. Importing Required Libraries**  

```python
import matplotlib.pyplot as plt
import seaborn as sns
```
- `matplotlib.pyplot` → For plotting.  
- `seaborn` → For advanced visualizations.  

---

### **2. Loading the Dataset**  

```python
data_load = sns.load_dataset("tips")
```
- Loads the **tips dataset**, which contains restaurant bills, tips, customer gender, day of the week, etc.  

---

### **3. Creating a FacetGrid**  

```python
fg = sns.FacetGrid(data_load, col="day", hue="sex")
```
- **`FacetGrid(data_load, col="day")`** → Creates **separate scatter plots for each day** (`"day"` column).  
- **`hue="sex"`** → Colors points **based on gender** (`"sex"` column).  

---

### **4. Mapping the Scatter Plot**  

```python
fg.map(plt.scatter, "total_bill", "tip").add_legend()
```
- **`.map(plt.scatter, "total_bill", "tip")`** → Plots a **scatter plot** with:  
  - **X-axis**: `total_bill` (total amount of the bill)  
  - **Y-axis**: `tip` (tip amount)  
- **`.add_legend()`** → Adds a **legend** showing color mapping for `"sex"`.  

---

### **5. Displaying the Plot**  

```python
plt.show()
```
- **Displays the final graph** with **multiple scatter plots**, one for each day.  

---

## **Output Example**  
This script will generate **four scatter plots**, one for each day (`Thur`, `Fri`, `Sat`, `Sun`).  
✅ **Each scatter plot shows the relationship between total bill and tip**  
✅ **Data points are colored based on gender (male/female)**  
✅ **A legend is included for gender identification**  

---

## **Conclusion**  
This script demonstrates how to use **Seaborn's FacetGrid** to:  
- **Create multiple plots for different categories (`col="day"`)**  
- **Use color to distinguish groups (`hue="sex"`)**  
- **Apply different plot types (`map(plt.scatter, x, y)`)**  

**FacetGrid** is useful for **comparing trends across different categories** in a dataset.  

---

Let me know if you need any modifications! 🚀
