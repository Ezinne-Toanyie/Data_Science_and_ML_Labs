# Week 4 - String Formatting, Control Flow, Functions & Pandas
**Program:** Data Science & Machine Learning

**Labs:** String Formatting & Control Flow | Functions | Introduction to Pandas

---

## Objective

To build on foundational Python knowledge by exploring string formatting techniques, control flow structures, reusable functions, and data manipulation with the Pandas library. These concepts are core building blocks for writing efficient, readable, and production-ready data science code.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Cloud-based notebook execution |
| Jupyter Notebook | Interactive coding environment |
| Pandas | Data manipulation and analysis library |
| Git and Github | Documentation |

---

## Step-by-Step Process

The lab was divided into four sections, each building on the previous.

---

### 1. String Formatting

String formatting allows text and variable values to be combined into clean, readable output. Three approaches were covered:

- **Concatenation** using the `+` operator; requires explicit type conversion with `str()` for non-string values.
- **f-strings (Formatted String Literals)**: the modern, preferred method. Variables are embedded directly inside `{}` within a string prefixed with `f`.
  >  ![String_formatting_1](https://i.postimg.cc/VkGMDPGH/String-1.png)
- **`.format()` method**: a flexible approach using placeholders `{}` that can be filled by position index, sequential order, or named keyword assignments.
  >  ![String_formatting_2](https://i.postimg.cc/NfLQRhXb/string-2.png)
  >  ![String_formatting_3](https://i.postimg.cc/mrjndkfH/string-3.png)
---

### 2. Control Flow

Control flow structures allow a program to make decisions and repeat actions based on conditions.

**Conditional Statements:**

| Statement | Behaviour |
|---|---|
| `if` | Executes a block only when the condition is `True` |
| `if-else` | Runs one block if `True`, another if `False` |
| Nested `if` | Checks additional conditions within an outer `if` block |
| `if-elif-else` | Tests multiple conditions in sequence; runs the first match |
| Ternary Operator | Writes a simple `if-else` on a single line |

>  ![Control_flow_1](https://i.postimg.cc/dVr3TPMz/control-flow-1.png)
>  ![Control_flow_2](https://i.postimg.cc/kgg9q0Jq/if-elif-else.png)
>  ![Control_flow_3](https://i.postimg.cc/D0w58P8G/nested-if.png)
>  ![Tenary_operators](https://i.postimg.cc/s22pPgVz/tenary-operators.png)


**Loops:**

| Loop | Behaviour |
|---|---|
| `for` loop | Iterates over each element in a sequence (list, dictionary, range, etc.) |
| `while` loop | Repeats a block of code as long as a condition remains `True` |
>  ![For_loop](https://i.postimg.cc/d1HNRfM4/for-loop.png)
>  ![For_loop_2](https://i.postimg.cc/V6xGHC6B/for-loop-2.png)
>  ![While_loop](https://i.postimg.cc/Pr4y1cmC/while-loop.png)

Practical loop examples included: filtering even numbers from a list, iterating over dictionary key-value pairs, computing a running total, and printing indexed list items.

---

### 3. Functions

A **function** is a reusable block of code that performs a specific task. Functions reduce repetition and make code easier to read and maintain.

**Standard Functions** are defined using the `def` keyword, can accept parameters, and return values using `return`. A function can return multiple values as a tuple, which are then accessed by index.
>  ![Function_1](https://i.postimg.cc/G26L7qGG/function-1.png)
>  ![Function_2](https://i.postimg.cc/q7Rpp9GF/function-2.png)

**Lambda Functions** are compact, single-expression functions defined inline using the `lambda` keyword, also called anonymous functions. They are best suited for short operations that don't require a full `def` block.
>  ![Lambda_function](https://i.postimg.cc/4NgZYK59/lambda.png)

**Some Built-in Functions** explored:

| Function | What It Does |
|---|---|
| `map(function, iterable)` | Applies a function to every item in an iterable and returns the results |
| `filter(function, iterable)` | Returns only the items from an iterable that satisfy a given condition |
| `reduce(function, iterable)` | Cumulatively applies a function to collapse an iterable into a single value |
| `sum(iterable)` | Returns the total of all numeric elements in an iterable |
| `max(iterable, key)` | Returns the largest item, optionally using a key function (e.g., `len`) |
| `min(iterable, key)` | Returns the smallest item, optionally using a key function |


---

### 4. Introduction to Pandas

**Pandas** is a Python library built for data manipulation and analysis. 
#### **Data Importing**

Data is loaded into Pandas using:

* `pd.read_csv()` → Import CSV files
  >  ![Import_csv](https://i.postimg.cc/xTdCfx3K/import-pd-1.png)
* `pd.read_excel()` → Import Excel files
  >  ![Import_xlsx](https://i.postimg.cc/Lsj4CrmJ/import-pd-2.png)

This is the first step in any real-world data analysis workflow.

  
Pandas has two primary data structures:

**Series**: a one-dimensional labelled array that can hold any data type. When a list contains mixed data types, Pandas assigns the output dataype as `object`.
>  ![Series](https://i.postimg.cc/rwTSZ99w/pd-1.png)

**DataFrame**: a two-dimensional labelled structure with rows and columns, similar to a spreadsheet or SQL table. DataFrames are created from Python dictionaries, where each key becomes a column name and its list of values forms the column data.
>  ![Dataframe](https://i.postimg.cc/wjFsfYvD/df-1.png)


**Data Cleaning & Preparation**

Data cleaning ensures the dataset is accurate and usable for analysis. It involves:
-  Handling missing values (e.g., filling or dropping nulls)
-  Converting data types for consistency
-  Removing duplicates or incorrect entries
-  Handling missing values
-  Converting data types where necessary
>  ![handling_null_values_1](https://i.postimg.cc/k5GzDShk/handling-missing-values.png)
>  ![handling_null_values_2](https://i.postimg.cc/HLFZxhMw/handing-missing-values-2.png)

**Data Aggregation**

Data aggregation summarizes data to extract meaningful insights.
-  Grouping data using groupby()
-  Applying summary functions like sum, mean, count
-  Comparing metrics across categories
>  ![grouping](https://i.postimg.cc/Ss0dqz08/grouping.png)

-Filtering data based on certain criteria
>  ![filterimg](https://i.postimg.cc/TwXVBMmk/filtering.png)
  
**Data Manipulation - Indexing & Slicing:**
- **Indexing** accesses a single element using its position (e.g., `s[0]`) or column name (e.g., `users['name'][2]`).
- **Slicing** retrieves a range of elements or a subset of columns from a DataFrame.
  
  >  ![Indexing_slicing](https://i.postimg.cc/pVZxnW1S/indexing-slicing.png)

**Data Combination - Concatenation:**

Pandas `pd.concat()` combines multiple DataFrames into one.

| Method | Behaviour |
|---|---|
| Vertical (`axis=0`) | Stacks DataFrames row-by-row (top to bottom) |
| Horizontal (`axis=1`) | Joins DataFrames column-by-column (left to right) |
| `keys` parameter | Labels each source DataFrame in the resulting multi-index |
| `ignore_index=True` | Resets the index after concatenation instead of preserving source labels |

>  ![vert_conc](https://i.postimg.cc/wjkbwMLP/vertical-conc.png)
>  ![hor_conc](https://i.postimg.cc/yxwTN49r/horizontal-conc.png)

After vertical concatenation with `keys`, rows can be accessed by label using `.loc[]`, and sliced across columns using label-based range notation.

---

## Key Observations & Lessons Learned

- f-strings are the cleanest and most readable string formatting method for most use cases; `.format()` offers more flexibility when formatting needs to be reused or dynamically constructed.
- The ternary operator is useful for simple conditional assignments but can reduce readability if overused. Standard `if-else` blocks are better for complex logic.
- Proper Indentation is a criteria for code blocks to run properly; especially in control flow and functions
- Lambda functions are best paired with `map()`, `filter()`, and `reduce()` for concise data transformations; they should not replace full functions where clarity matters.
- `reduce()` must be explicitly imported from `functools` .
- A Pandas DataFrame is essentially a dictionary of lists under the hood, which reinforces why dictionary literacy (covered in prior weeks) is foundational for data science.
- Vertical concatenation with `keys` creates a multi-index structure, which enables precise row selection using `.loc[]`. This is an important pattern for working with layered datasets.

---

## 📁 Repository Structure

```
Week_4
 ┣ README.md
 ┣ String_and_Control_Flow.ipynb
 ┣ Functions.ipynb
 ┗ Pandas_Notebook.ipynb
```

---

## 🔗 Connect With Me

**[www.linkedin.com/in/ezinne-toanyie](http://www.linkedin.com/in/ezinne-toanyie)**

This lab is part of an ongoing learning journey in Data Science & Machine Learning courtesy ParoCyber. Follow along as I document each week's progress.
