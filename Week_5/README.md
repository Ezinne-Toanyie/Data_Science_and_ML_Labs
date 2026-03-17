# Week 5 - NumPy & Data Visualization
**Program:** Data Science & Machine Learning

**Labs:** NumPy | Visualization in Python (Matplotlib & Seaborn)

---

## Objective
This week introduced NumPy for numerical computing and covered data visualization using Matplotlib and Seaborn.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Python | Programming language |
| Google Colab | Cloud-based notebook execution |
| Jupyter Notebook | Interactive coding environment |
| NumPy | Numerical array computation |
| Matplotlib | Static and custom data visualization |
| Seaborn | Statistical and high-level visualization |
| Git and Github | Documentation |

---

## Step-by-Step Process

The lab was divided into two sections, each building on the previous.

### 1. NumPy

NumPy is a Python library for working with numbers stored in arrays. It is fast, efficient, and widely used in data science.

**Array Creation**

Arrays can be created from Python lists as 1-Dimensional or 2-Dimensional structures. `np.zeros()` creates an array of a given size filled with zeros.

>  ![numpy_1](https://i.postimg.cc/VNsPr4Nc/numpy-1.png)
>  ![numpy_2](https://i.postimg.cc/sgctrSJf/numpy-2.png)



**Array Attributes**

| Attribute | What It Returns |
|-----------|----------------|
| `.shape` | Number of rows and columns |
| `.size` | Total number of elements |
| `.dtype` | Data type of the elements |

>  ![array_shape](https://i.postimg.cc/5yQD8Rvp/shape-size.png)
>  ![array_datatype](https://i.postimg.cc/x1QTTvDp/datatype.png)



**Array Operations**

Basic math (+, −, ×) applies to every element in the array at once. No need to loop through each item.

>  ![array_ops](https://i.postimg.cc/gkWPvGS3/array-operations-1.png)



**Aggregation Functions**

| Function | What It Does |
|----------|--------------|
| `.sum()` | Adds all elements |
| `.max()` | Returns the largest value |
| `.min()` | Returns the smallest value |

>  ![array_aggregation](https://i.postimg.cc/6pqbZSXL/numpy-aggregation.png)



**Indexing & Slicing**

Use `[row_start:row_end, col_start:col_end]` to select specific rows and columns from an array.

>  ![array_indexing](https://i.postimg.cc/TwVtGvr0/numpy-indexing.png)



**Array Manipulation**

| Method | What It Does |
|--------|--------------|
| `.reshape(r, c)` | Changes the array shape without changing its values |
| `np.concatenate()` | Joins two or more arrays together |
| `np.append()` | Adds values to the end of an array |
| `np.delete()` | Removes an element at a given index |

>  ![array_reshape](https://i.postimg.cc/fRYt8WDs/reshaping.png)
>  ![array_conc](https://i.postimg.cc/XJ1prpcC/conc-arrays.png)
>  ![array_delete](https://i.postimg.cc/jjs5vzMx/deleting-array.png)



**Broadcasting**

Broadcasting lets NumPy apply an operation between arrays of different sizes. It automatically stretches the smaller value to match the larger array. No manual reshaping is needed.

>  ![broadcasting](https://i.postimg.cc/hhW4mxJP/Broadcasting.png)



**Random Number Generation**

| Function | What It Does |
|----------|--------------|
| `np.random.rand()` | Random floats between 0 and 1 |
| `np.random.randint()` | Random whole numbers within a range |
| `np.random.randn()` | Random numbers from a normal distribution |
| `np.random.choice()` | Randomly picks items from an array |

>  ![random_1](https://i.postimg.cc/nz9CQnd5/random-number-generation.png)
>  ![random_2](https://i.postimg.cc/kgj412zc/random-numbers-2.png)



**Linear Algebra**

NumPy supports standard matrix operations: addition, subtraction, element-wise multiplication, matrix multiplication (`@` or `np.matmul()`), dot product (`np.dot()`), transpose (`np.transpose()`), inverse (`np.linalg.inv()`), determinant (`np.linalg.det()`), and identity matrix (`np.eye()`).

>  ![linalg-1](https://i.postimg.cc/nVYnSsQ3/linalg-1.png)
>  ![linalg-2](https://i.postimg.cc/wBmpX3p7/linalg-2.png)
>  ![linalg-3](https://i.postimg.cc/8PzgyZGk/linalg-3.png)
>  ![linalg-4](https://i.postimg.cc/25vsqJQb/linalg-4.png)



**Statistical Functions**

| Function | What It Does |
|----------|--------------|
| `np.mean()` | Calculates the average |
| `np.median()` | Finds the middle value |
| `np.std()` | Measures how spread out the values are |
| `stats.mode()` | Finds the most frequent value (requires `scipy.stats`) |

>  ![stats_1](https://i.postimg.cc/WbHC5jSh/stats-1.png)
>  ![stats_2](https://i.postimg.cc/qq7DGZ32/stats-2.png)

---

### 2. Visualization in Python

**Matplotlib**

Matplotlib is a Python library for creating charts and graphs. It gives full control over how a plot looks.

| Chart Type | When to Use It |
|-----------|----------------|
| Bar Chart | Comparing values across categories |
| Grouped Bar Chart | Comparing sub-groups within categories |
| Pie Chart | Showing how parts make up a whole |
| Histogram | Seeing how values are spread out |
| Line Plot | Showing change over time or a sequence |

Key customisation tools used: `figsize`, `plt.title()`, `plt.xlabel()`, `plt.ylabel()`, `plt.xticks(rotation=)`, `plt.grid()`, and `plt.tight_layout()`.

**Seaborn**

Seaborn is built on top of Matplotlib. It creates polished statistical charts with less code.

| Chart Type | When to Use It |
|-----------|----------------|
| Count Plot | Comparing how often categories appear |
| Pair Plot | Seeing relationships between all numeric columns at once |
| Heatmap | Showing correlations using colour |
| Box Plot | Displaying spread, median, and outliers |
| Joint Plot | Exploring the relationship between two variables |
| Violin Plot | Combining a box plot with a distribution curve |

The `hue` parameter adds a colour dimension based on a category. This makes it easy to spot patterns across groups without creating separate charts.

---

## Key Observations & Lessons Learned

- NumPy is faster than Python lists for number manipulation. It processes all elements at once instead of one by one.
- Broadcasting removes the need to reshape arrays before doing math. It keeps code shorter and easier to read.
- NumPy does not have a built-in mode function. `scipy.stats.mode()` must be imported separately.
- Matplotlib gives more control but needs more code.
- Seaborn is quicker for standard statistical charts.
- The `hue` parameter in Seaborn adds a third variable to a chart using colour. It removes the need to split data into separate plots.
- Pair plots and heatmaps are great starting points in any analysis. They quickly show patterns and relationships across variables.

---

## 📁 Repository Structure

```
Week_5
 ┣ README.md
 ┣ Numpy_Notebook.ipynb
 ┗ Visualization_in_Python.ipynb
```

---

## 🔗 Connect With Me

[www.linkedin.com/in/ezinne-toanyie](https://www.linkedin.com/in/ezinne-toanyie)

*This lab is part of an ongoing learning journey in Data Science & Machine Learning courtesy ParoCyber. Follow along as I document each week's progress.*
