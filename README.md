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
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solutions%20to%20question%202.png)
- The first query shows how many times a customer ordered using the count of order_date
- Due to the fact that some customers ordered twice in one day, I used *DISTINCT* to pick out only one of the duplicate days to know the actual count of days a customer visited.

### Question 3: First Item Purchased by Each Customer
Query to find the first item from the menu purchased by each customer:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solution%20to%20question%203.png)
- I wrote a subquery to rank order date by ascending order and partition the ranking by customer ID
- To get all columns useful for my solution I joined the sales table and the Menu table
- Then the main Query was to fetch the lowest rank
- More Information was required for example a time stamp for products bought on the same day, this way we know which was ordered first  
### Question 4: Most Purchased Item and Purchase Count
To answer the question "What is the most purchased item on the menu and how many times was it purchased by all customers?"
- I wrote a query to get the number of times each product was purchased
- I wrote a second query to check the number of times the most purchased product was bought by each customer.

Query to identify the most purchased item on the menu and its purchase count:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solution%20to%20question%204.png)
### Question 5: Most Popular Item for Each Customer
Query to find the most popular item for each customer:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/Solution%20to%20question%205.png)
### Question 6: First Item Purchased After Becoming a Member
To answer question 6
- I joined all three tables, I used a right join for the third table so I only get information from the left table that matches information in the right table.
- I ranked order date by ascending order and partitiion the ranking by customer ID
- I also used the **_WHERE clause_** with **_operators_** to reference the the join date from the membership table
Query to identify the item purchased first by a customer after becoming a member:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/Solution%20to%20question%206.png)
### Question 7: Item Purchased Just Before Becoming a Member
Query to find the item purchased just before a customer became a member:
I followed the step as outlined in question 6, with a few changes to the **_operators_**
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solution%20to%20question%207.png)
### Question 8: Total Items and Amount Spent Before Membership
- From the question the interest is on the customers that became members
- I got their total items and the total amount spent

Query to calculate the total items and amount spent by each member before becoming a member:
![](https://github.com/AnietieJohnson/Danny-Ma-week-1-challenge-/blob/main/solutions%20to%20question%208.0.png)
## Conclusion
This SQL analysis of the Danny Ma challenge questions provided valuable insights into customer behaviors, purchase patterns, and membership dynamics at the restaurant. By structuring queries to address each specific question, we gained a comprehensive understanding of the dataset and derived meaningful conclusions from it.
## Limitations
- The analysis relies on the accuracy and completeness of the dataset. Any missing or incorrect data may affect the results.
- Order date can be specified with time for better analysis  
