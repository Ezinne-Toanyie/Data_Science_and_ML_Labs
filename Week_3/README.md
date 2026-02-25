# Week 3 - Data Structures in Python (Part 2) & String Operations
**Program:** Data Science & Machine Learning

**Labs:** Data Structures – Operators | String Methods & Dataflow

---

## Objective

To build on the foundational Python concepts from Week 2. This week covers how Python evaluates, compares, and transforms data. These skills are essential for writing logic, filtering datasets, and processing text in data science workflows.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Cloud-based notebook execution |
| Jupyter Notebook | Interactive coding environment |
| Git and Github | Documentation |

---

## Step-by-Step Process

The labs were divided into two notebooks, each covering a distinct set of Python concepts with hands-on practice.

---

### 📘 Notebook 1: Data Structures – Part 2: Operators

#### 1. Arithmetic Operators

Arithmetic operators perform standard mathematical calculations on numeric values.

| Operator | What It Does |
|---|---|
| `+` | Addition — returns the sum of values |
| `-` | Subtraction — returns the difference between values |
| `*` | Multiplication — returns the product of values |
| `/` | Division — always returns a float, even for whole-number results |
| `//` | Floor Division — divides and discards the remainder, returning an integer |
| `%` | Modulo — returns only the remainder after division |
| `**` | Exponentiation — raises a number to the power of another |


**Commands Executed:**

```python
>[Arithmetic_Operators_1] (https://i.postimg.cc/yxbF6JpK/Arithmetic-operators-1.png)
```

---

#### 2. Comparison Operators

Comparison operators evaluate two values and return a boolean result (`True` or `False`).

| Operator | What It Does |
|---|---|
| `>` | Greater than |
| `<` | Less than |
| `==` | Equal to |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `!=` | Not equal to |

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

---

#### 3. Logical Operators

Logical operators combine multiple conditions and return a single boolean result.

| Operator | What It Does |
|---|---|
| `and` | Returns `True` only if **all** conditions are `True` |
| `or` | Returns `True` if **at least one** condition is `True` |
| `not` | Reverses the boolean result of a condition |

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

---

#### 4. Assignment Operators

Assignment operators update a variable's value by performing an operation and reassigning the result in a single step.

| Operator | What It Does |
|---|---|
| `+=` | Adds a value to `x` and reassigns the result |
| `-=` | Subtracts a value from `x` and reassigns the result |
| `*=` | Multiplies `x` by a value and reassigns the result |
| `/=` | Divides `x` by a value and reassigns the result |
| `//=` | Performs floor division on `x` and reassigns the result |
| `**=` | Raises `x` to a power and reassigns the result |

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

---

#### 5. Bitwise Operators

Bitwise operators work on the binary representation of integers. Python's `bin()` function can be used to view the binary equivalent of any number.

| Operator | Symbol | What It Does |
|---|---|---|
| AND | `&` | Returns bits that are `1` in **both** numbers |
| OR | `\|` | Returns bits that are `1` in **either** number |
| XOR | `^` | Returns bits that are `1` in **one but not both** numbers |
| NOT | `~` | Flips all bits (bitwise negation) |
| Right Shift | `>>` | Shifts bits to the right by a specified number of positions |
| Left Shift | `<<` | Shifts bits to the left by a specified number of positions |

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

---

#### 6. Membership Operators

Membership operators check whether a value exists within a sequence such as a list or string. Python provides two: `in` and `not in`.

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

---

#### 7. Identity Operators

Identity operators check whether two variables point to the **same object in memory** — not just whether they hold equal values. Python provides two: `is` and `is not`.

> **Key Distinction:** Two lists with identical values are **equal** (`==`) but are **not** the same object in memory (`is` returns `False`), because Python creates them as separate objects.

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

---

### 📗 Notebook 2: String Methods & Dataflow

A **string** is a sequence of characters used to represent text. Strings in Python are immutable — operations on them return new strings rather than modifying the original.

The following string methods were explored:

#### Case & Type Checking Methods

| Method | What It Does |
|---|---|
| `upper()` | Converts all characters to uppercase |
| `lower()` | Converts all characters to lowercase |
| `isalpha()` | Returns `True` if all characters are alphabetic (no spaces or numbers) |
| `isdigit()` | Returns `True` if all characters are numeric digits |
| `islower()` | Returns `True` if all characters are lowercase |
| `isupper()` | Returns `True` if all characters are uppercase |

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

#### Manipulation & Search Methods

| Method | What It Does |
|---|---|
| `split()` | Separates a string into a list using a specified delimiter |
| `join()` | Merges a list of strings into one, using a specified separator |
| `replace()` | Substitutes a specified substring with a new value |
| `startswith()` | Returns `True` if the string begins with a specified character or substring |
| `endswith()` | Returns `True` if the string ends with a specified character or substring |

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

**Commands Executed:**

```python
# Add your screenshots or code snippets here
```

> **Note:** String methods like `isalpha()` are case-sensitive and space-sensitive. `"ParoCyber LLC"` returns `False` for `isalpha()` because it contains a space.

---

## Key Observations & Lessons Learned

- Arithmetic operators follow standard mathematical precedence — use parentheses to control evaluation order where needed.
- Standard division `/` always returns a float; use `//` when integer output is required, and `%` to capture the remainder.
- Logical operators (`and`, `or`, `not`) are the foundation of conditional logic and data filtering in Python.
- Assignment operators make code more concise and are commonly used in loops and iterative calculations.
- Bitwise operators work at the binary level and are particularly useful in low-level data manipulation, networking, and certain algorithmic problems.
- Identity operators (`is` / `is not`) test memory location, not value equality — two objects can be equal in value but distinct in memory.
- String methods do not modify the original string; they return a new one. This reinforces the concept of string immutability.
- `isalpha()` returns `False` for strings containing spaces, numbers, or special characters — a common source of confusion when validating text data.
- `split()` and `join()` are complementary methods that convert between strings and lists, which is fundamental for text parsing and data wrangling tasks.

---

## 📁 Repository Structure

```
Week_3
 ┣ README.md
 ┣ Data_Structures_-_Part_2.ipynb
 ┗ String_and_Dataflow.ipynb
```

---

## 🔗 Connect With Me

**[www.linkedin.com/in/ezinne-toanyie](https://www.linkedin.com/in/ezinne-toanyie)**

This lab is part of an ongoing learning journey in Data Science & Machine Learning courtesy of ParoCyber. Follow along as I document each week's progress.
