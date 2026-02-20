# Week 2 - Data Structures in Python

> **Program:** Data Science & Machine Learning
>
> **Lab:** Data Structures - Lists, Tuples & Dictionaries

---

## Objective

To explore data structures in Python programming language and understand how to store, access, modify, and manage collections of data. This lab covers the key operations used on Lists, Tuples, and Dictionaries. These are foundational structures for data manipulation in data science workflows.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Python | Programming language |
| Google Colab | Cloud-based notebook execution |
| Jupyter Notebook | Interactive coding environment |
| Git and Github | Documentation |

---

## Step-by-Step Process

The lab was divided into three sections, each covering a different data structure with hands-on practice.

---

### 1. Lists

A list is an ordered, changeable collection of items(elements). Elements can be added, removed, rearranged, or counted at any time.

* Lists are created using square brackets `[]`.
* Items in a list are assigned index numbers starting from `0`.
* When duplicate items exist, operations like `remove()` follow a **first-in, first-out** rule.

The following methods were explored:

| Method | What It Does |
|--------|-------------|
| `append()` | Adds one item to the end of the list |
| `extend()` | Merges another list into the existing list |
| `insert()` | Adds an item at a specific index position |
| `remove()` | Deletes the first occurrence of a specified item |
| `index()` | Returns the position number of a specified item |
| `pop()` | Removes and returns the item at a given index |
| `count()` | Counts how many times an item appears |
| `sort()` | Arranges items in ascending (A–Z) order |
| `reverse()` | Flips the current order of items in the list |

**Commands Executed:**

>  ![List 1](https://i.postimg.cc/JzSPGwBD/1.png)
>  ![List 2](https://i.postimg.cc/DzB0xhdQ/2.png)
>  ![List 3](https://i.postimg.cc/GphGLqX7/3.png)
>  ![List 4](https://i.postimg.cc/SNF92yZn/4.png)
>  ![List 5](https://i.postimg.cc/HnQV4y6K/5.png)

---

### 2. Tuples

A tuple is an ordered collection of items that **cannot be modified** after creation. It is ideal for storing data that should remain fixed and protected from accidental changes.

* Tuples are created using parentheses `()`.
* Unlike lists, tuples do not support `append()`, `remove()`, or `sort()`.
* Tuple elements can still be accessed, counted, and indexed.

**Commands Executed:**

> ![Tuples](https://i.postimg.cc/SxtN9dyf/TUPLE.png)

---

### 3. Dictionaries

A dictionary stores data as **key-value pairs**. Like a lookup table, each key acts as a unique label and maps to its associated value. Dictionaries were used in this lab to store personal profile data and a structured employee records dataset.

* There are three ways to create a dictionary: curly brace notation `{}`, `dict()` with keyword arguments, and `dict()` with a list of tuples.
* Values are retrieved using `get()` or bracket notation `[]`.
* The `employees` dictionary, used in this lab, demonstrates how real-world tabular data is structured in Python.

The following methods were explored:

| Method | What It Does |
|--------|-------------|
| `get()` | Retrieves the value associated with a specified key |
| `keys()` | Returns all keys in the dictionary |
| `values()` | Returns all values in the dictionary |
| `items()` | Returns all key-value pairs in the dictionary |
| `update()` | Modifies an existing value or adds a new key-value pair |

**Commands Executed:**

> ![Dict_1](https://i.postimg.cc/LsLKs3hm/dict-1.png)
> ![Dict_2](https://i.postimg.cc/HnPPzrVH/GET-dict-2.png)
> ![Dict_3](https://i.postimg.cc/0jrVz9ZK/EMPLOYEES-DICT-3.png)
> ![Dict_4](https://i.postimg.cc/TPGQrVCK/ITEMS-KEYS-VALUES-4.png)
> ![Dict_5](https://i.postimg.cc/8zdmPFND/UPDATE-5.png)

---

## Key Observations & Lessons Learned

- A **list** is used when data needs to be frequently added, removed, or rearranged.
- A **tuple** is best used for fixed reference data (e.g., constants) that should not be altered. Its immutability protects data integrity.
- **Dictionaries** with lists as values is a foundational pattern for handling tabular data in Python.
- The `remove()` method only deletes the **first occurrence** of a duplicate item; understanding this behaviour prevents silent data errors.
- Knowing all three dictionary creation methods adds flexibility when working with data from different sources such as APIs, CSV files, and databases.

---

## 📁 Repository Structure

```
 Week_2
 ┣ README.md
 ┗ Week 2 - Data Structures.ipynb
```

## 🔗 Connect With Me

> www.linkedin.com/in/ezinne-toanyie

---

*This lab is part of an ongoing learning journey in Data Science & Machine Learning courtesy ParoCyber.*
*Follow along as I document each week's progress.*
