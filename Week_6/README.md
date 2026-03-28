# Week 6 - Exploratory Data Analysis
**Program**: Data Science & Machine Learning

**Lab**: Exploratory Data Analysis(EDA)

## Objective

Exploratory Data Analysis(EDA) is a crucial step in Data Science that involves summarizing and visualizing the important characteristics of a dataset.

This process helps in understanding the data, detecting anomalies and identifying patterns.

This lab presents an exploratory data analysis (EDA) of a synthetic Fintech SaaS dataset. The dataset simulates a subscription-based fintech platform with information on customer usage, transactions, support interactions, and revenue.

 The goal is to understand customer behavior, identify key revenue drivers, and uncover factors contributing to customer churn.
 
---

## Tools Used

| Tool | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Cloud-based notebook execution |
| Jupyter Notebook | Interactive coding environment |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Matplotlib | Plotting and visualization |
| Seaborn | Statistical data visualization |
| Git and Github | Documentation |
ChatGPT  | Generating Synthetic dataset  |

---

## The Dataset

The dataset is a synthetic Fintech SaaS platform just like a fictional subscription-based financial software company.

Each row represents a customer, with details on:

- Their subscription tier
- How long they have been a customer (tenure)
- How many transactions they make
- Monthly revenue they generate
- Support tickets they have raised
- Whether they eventually churned (left) or stayed

Before any analysis could begin, the data needed to be cleaned.

---

## Step-by-Step Process

### 1. Loading the Data

The dataset was loaded using `pd.read_csv()` and quickly inspected using `.head()` and `.tail()` to get a feel for its structure.

> ![Loading the dataset](https://i.postimg.cc/t4Q2TNGs/loading-the-dataset.png)
> ![Loading the dataset_2](https://i.postimg.cc/xTr4J2LW/loading-the-dataset-2.png)

---

### 2. Initial Data Inspection

- `.info()` revealed the column names, data types, and how many values were missing
- `.describe(include='all')` gave a statistical summary of both numerical and categorical columns


> ![Data info output](https://i.postimg.cc/KYPJXkKy/inspecting-the-data.png)
> ![Data describe output](https://i.postimg.cc/wjKX6x84/data-inspection-2.png)

This step answered the first question: *What are we actually working with?*

---

### 3. Summary Statistics

Two separate summaries were generated:

- **Numerical columns**: mean, min, max, standard deviation
- **Categorical columns**: unique value counts and the most frequent values


> ![Numerical_Summary statistics](https://i.postimg.cc/7YXGfSRB/numerical-summary.png)
> ![Categorical_Summary statistics](https://i.postimg.cc/WbptLh45/categorical-summary.png)

This helped paint a quick picture of the range and spread of the data.

---

### 4. Missing Values Analysis

Missing values were intentionally introduced into the dataset to simulate real-world data quality issues and demonstrate data cleaning techniques.

`df.isnull().sum()` was used to count missing values in each column.
Several columns had `null` values; these needed to be addressed before drawing any conclusions.

![Missing values analysis](https://i.postimg.cc/KY1MX40b/missing-value-analysis.png)

---

### 5. Data Cleaning

Rather than deleting rows with missing data (which wastes information), smart imputation was used:

- **Monthly fee** column was filled with the **median** (less sensitive to extreme values)
- **Tenure & transaction value** column was filled with the **mean**
- **Subscription tier** column was filled with the **most common value(mode)**
- **Region & marketing channel** column was filled with `"Unknown"`
- **Marketing channel** was eventually **dropped** just for demonstration purposes

A final `df.isnull().sum()` confirmed zero missing values remained.

> ![Data cleaning](https://i.postimg.cc/Hk9gptPh/data-cleaning-1.png)
> ![Data cleaning verification](https://i.postimg.cc/wxLb8jrJ/data-cleaning-2.png)
> ![Dropping_column](https://i.postimg.cc/WbKDGs26/column-drop.png)

---

## Data Visualization

With the data cleaned, the real exploration began. Nine visualizations were developed, each designed to answer a specific business question.

---

### 1. Who generates the most revenue?

![Revenue distribution histogram](https://i.postimg.cc/QtsSjpw8/Distribution-of-Monthly-Revenue.png)

The histogram shows the distribution of monthly revenue appears right-skewed, indicating that a large proportion of customers generate relatively low revenue, while a smaller group of high-value customers contribute disproportionately to total revenue. 

This pattern is typical in SaaS businesses, where enterprise clients drive significant revenue.

---

### 2. Does subscription tier affect revenue?

![Average revenue by subscription tier](https://i.postimg.cc/76d3f0QW/Revenue-by-Subscription-Tier.png)

The average revenue varies significantly across subscription tiers, with higher-tier plans contributing more revenue per customer. 

This suggests that upgrading customers to premium tiers could be a key strategy for increasing overall revenue.

---

### 3. How many customers have churned?

![Churn distribution bar chart](https://i.postimg.cc/fysb2b3V/Churn-Distribution.png)

The churn distribution chart shows that **most customers are still active**. The platform is generally stable.

But the churned group is not negligible. And since retaining a customer is cheaper than acquiring a new one, even a small churn rate deserves attention.

---

### 4. Do long-term customers pay more?

![Tenure vs monthly revenue scatter plot](https://i.postimg.cc/B6qym9SQ/Tenure-vs-Monthly-Revenue.png)

The scatter plot of tenure vs. revenue shows a **positive trend** ; customers who have been around longer tend to generate more revenue.

This implies that loyal customers are more likely to upgrade, transact more, and refer others. **The longer you keep a customer, the more valuable they become.**

This reinforces the importance of customer retention strategies in driving revenue growth.

---


### 5. Which regions perform best?

![Average revenue by region bar chart](https://i.postimg.cc/QdCck6G2/Revenue-by-Region.png)

Revenue varies across regions, highlighting geographical differences in customer value. 
Some regions contribute more significantly to revenue, which may reflect differences in market maturity, pricing sensitivity, or customer behavior.

---

### 6. Are unhappy customers more likely to leave?

![Support tickets by churn status boxplot](https://i.postimg.cc/Xv077J8J/Customer-Support-Tickets-by-Churn.png)

The box plot tells a striking story: **customers who churned had significantly more support tickets** than those who stayed.

This suggests that unresolved issues and frustrating experiences push customers toward the exit. Better support could directly reduce churn.


---

### 7. What variables are most connected to revenue?

The correlation heatmap maps out how strongly each variable relates to revenue.

![Correlation heatmap](https://i.postimg.cc/CxCp74GL/Correlation-matrix.png)

**Transactions and active users** show the highest positive correlation with monthly revenue. Features like region (categorical) show weaker direct correlation.
This helps narrow down which variables will matter most if a predictive model is built later.


---

### 8. How do key features relate to each other?

![Pairplot of key features](https://i.postimg.cc/5ycMpKRL/Pairplot.png)

The pairplot displays scatter plots for every combination of tenure, transactions, active users, and revenue all at once.

Visible clusters and upward trends across multiple panels confirm that **these features move together in meaningful ways**. They're not random; they tell a consistent story about customer value.


---

## Key Insights

* A small group of high-value customers drives most of the revenue 
* Higher subscription tiers generate significantly more average revenue 
* Transaction frequency is one of the strongest predictors of revenue 
* Long-tenured customers are more valuable; retention pays off over time 
* Customers with many support tickets are more likely to churn 
* Revenue performance varies by region; markets behave differently 
* Active user count and transactions are the most correlated features with revenue 

---

## Repository Structure

```
Week_6
 ┣ README.md
 ┗ Exploratory_Data_Analysis.ipynb
 ┗ fintech_saas_dataset.csv
```

---

## 🔗 Connect With Me

**www.linkedin.com/in/ezinne-toanyie**

This lab is part of an ongoing learning journey in Data Science & Machine Learning courtesy ParoCyber. Follow along as I document each week's progress.
