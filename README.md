# Danny Ma Challenge: SQL Analysis Documentation
## Introduction
This documentation presents the SQL analysis of the Danny Ma challenge questions involving a restaurant dataset. The dataset contains information about customer transactions, menu items, membership status, and dates of visits. The goal is to derive insights by answering specific questions through SQL queries.
## Data Source
The dataset provided for this analysis includes the following tables:
**Sales:** Contains information about customer's order including customer ID, Order Date, Product ID.
**Menu:**  Lists the Product Price with their corresponding Product ID and  Product Name.
**Members**:Contains details about customer who are members this includes Customer ID and Join Date
## Questions and Solutions
### Question 1: Total Amount Spent by Each Customer
Query to calculate the total amount each customer spent at the restaurant:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solution%20to%20question%201.png)
### Question 2: Number of Days Each Customer Visited the Restaurant
Query to count the number of days each customer visited the restaurant:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/Answer%20to%20question%202.png)
- The first query shows how many times a customer ordered using the count of order_date
- Due to the fact that some customers ordered twice in one day, I used *DISTINCT* to pick out only one of the duplicate days to know the actual count of days a customer visited.
### Question 3: First Item Purchased by Each Customer
Query to find the first item from the menu purchased by each customer:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solution%20to%20question%203.png)
