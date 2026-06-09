# Customer Segmentation using RFM Analysis

## Overview

This project focuses on Customer Segmentation using transactional retail data. The objective is to identify customer purchasing behavior patterns and create meaningful customer segments using Recency, Frequency, and Monetary (RFM) analysis.

Customer segmentation helps businesses improve marketing strategies, customer retention, personalization, and revenue generation by targeting customers based on their purchasing habits.

---

## Business Problem

Businesses often have thousands of customers with different purchasing behaviors. Treating all customers equally leads to inefficient marketing campaigns and reduced customer engagement.

This project answers the following questions:

* Who are the most valuable customers?
* Which customers purchase frequently?
* Which customers are at risk of churn?
* How recently have customers interacted with the business?
* How much revenue does each customer contribute?

---

## Dataset Information

The dataset contains retail transaction records with the following attributes:

| Feature     | Description                   |
| ----------- | ----------------------------- |
| InvoiceNo   | Unique transaction identifier |
| StockCode   | Product code                  |
| Description | Product description           |
| Quantity    | Quantity purchased            |
| InvoiceDate | Transaction date and time     |
| UnitPrice   | Product unit price            |
| CustomerID  | Unique customer identifier    |
| Country     | Customer country              |

Dataset Summary:

* Total Records: 375,187+
* Features: 8
* Multiple countries represented
* Transaction period spans approximately one year

---

## Project Workflow

### 1. Data Loading

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

Dataset imported using Pandas and inspected for structure, data types, and missing values.

---

### 2. Data Preprocessing

The following preprocessing steps were performed:

* Converted InvoiceDate to datetime format
* Created transaction amount:

```python
Amount = Quantity × UnitPrice
```

* Calculated invoice-level total sales
* Aggregated customer transactions
* Removed inconsistencies and prepared customer-level dataset

---

### 3. Feature Engineering

Generated customer-level metrics:

#### Monetary Value

Total spending by each customer.

```python
Monetary = Sum(Transaction Amount)
```

#### Frequency

Number of purchases normalized by customer lifetime.

```python
Frequency = Number of Purchases / Customer Lifetime
```

#### Recency

Days since last purchase.

```python
Recency = Latest Date - Last Purchase Date
```

#### Customer Lifetime

Calculated using:

```python
Customer Lifetime = Last Purchase Date - First Purchase Date
```

---

### 4. RFM Analysis

Three important customer behavior metrics were created:

| Metric    | Meaning                         |
| --------- | ------------------------------- |
| Recency   | How recently customer purchased |
| Frequency | How often customer purchases    |
| Monetary  | How much customer spends        |

These metrics form the foundation of customer segmentation.

---

## Technologies Used

| Tool             | Purpose                   |
| ---------------- | ------------------------- |
| Python           | Programming Language      |
| Pandas           | Data Manipulation         |
| NumPy            | Numerical Computation     |
| Matplotlib       | Visualization             |
| Seaborn          | Statistical Visualization |
| Jupyter Notebook | Development Environment   |

---

## Project Structure

```text
Customer-Segmentation/
│
├── data/
│   └── sales_customer_segmentation.csv
│
├── notebooks/
│   └── Customer_Segmentation.ipynb
│
├── README.md

```

---

## Key Metrics Created

### Recency

Measures customer activity freshness.

Lower recency value indicates:

* Active customer
* Higher retention probability
* Better engagement

---

### Frequency

Measures purchasing consistency.

Higher frequency indicates:

* Repeat customers
* Loyal customers
* Strong customer relationship

---

### Monetary

Measures customer value.

Higher monetary value indicates:

* High-value customers
* Revenue-driving customers
* Premium customer segment

---

## Business Applications

This customer segmentation framework can be used for:

### Customer Retention

Identify customers likely to churn and take preventive action.

### Personalized Marketing

Design campaigns specific to customer segments.

### Loyalty Programs

Reward high-value customers appropriately.

### Revenue Optimization

Focus acquisition and retention efforts on profitable customers.

### Customer Lifetime Value Enhancement

Improve long-term customer profitability.

---

## Sample Customer Segments

| Segment             | Characteristics                          |
| ------------------- | ---------------------------------------- |
| Champions           | Recent, frequent, high spenders          |
| Loyal Customers     | Frequent buyers with consistent spending |
| Potential Loyalists | Recently acquired customers              |
| At Risk             | Previously active but inactive recently  |
| Lost Customers      | Long inactive customers                  |
| Big Spenders        | High monetary contribution               |

---

## Future Improvements

* Automated RFM scoring
* K-Means customer clustering
* Customer Lifetime Value (CLV) prediction
* Churn prediction model
* Interactive dashboard using Power BI/Tableau
* Marketing recommendation engine

---

## Results

The project successfully transforms raw transactional data into customer-level behavioral metrics, enabling businesses to understand customer value and create targeted marketing strategies.

The generated RFM features provide a strong foundation for advanced customer analytics and machine learning-based segmentation.

---

## Author

**Vaibhav Solanke**

Customer Segmentation using RFM Analysis and Retail Transaction Data.

---

## License

This project is intended for educational, analytical, and business intelligence purposes.
