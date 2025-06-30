# TASK-5
# E-commerce SQL Joins

## Tables
- Customers
- Orders

## Joins

1. INNER JOIN – Customers with orders
2. LEFT JOIN – All customers, even if no order
3. RIGHT JOIN – All orders, even if no customer
4. FULL OUTER JOIN – All customers + orders

🛒 E-commerce SQL Joins – Simple Project
This project is made to understand how SQL joins work using a basic e-commerce example. We use two simple tables: Customers and Orders.

The Customers table stores customer details like customer ID, name, and city.
The Orders table stores order details like order ID, customer ID, amount, and status.

We entered some sample data. For example, Alice and Bob are customers who placed orders. Charlie is a customer who didn’t place any order. There is also one order placed by an unknown customer (to test missing data cases).

🔗 Understanding the Joins
1. INNER JOIN
This join shows only the customers who actually placed orders.
If a customer didn’t place any order, they will not appear in the result.
In our case, only Alice and Bob appear. Charlie is not shown because he has no order.

2. LEFT JOIN
This join shows all customers, whether they placed an order or not.
If there’s no order, the order details will be shown as blank or NULL.
So Alice, Bob, and Charlie all appear. Charlie’s order columns show NULL since he didn’t place any order.

3. RIGHT JOIN
Right join shows all orders, even if they don't match with a customer.
Since SQLite doesn’t support RIGHT JOIN directly, we use a similar logic by joining from the orders side.
In this case, we also see an order placed by a customer who doesn’t exist in the customer list (customer_id 4).

4. FULL OUTER JOIN
This join combines both LEFT and RIGHT JOIN. It shows all customers and all orders — even if they don’t match.
This is useful when we want to see everything in one result, no matter if there’s a match or not.
Charlie appears (no order), and the order from customer_id 4 also appears (no matching customer).


