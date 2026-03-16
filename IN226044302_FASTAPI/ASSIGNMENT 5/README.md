FastAPI Assignment 5 – Day 6

The objective of this assignment was to implement advanced API features such as **searching, sorting, and pagination** using FastAPI. The APIs were tested using Swagger UI to verify correct responses and functionality.

Question 1 – Product Search (GET)

Endpoint used:

GET /products/search

The search API was tested with different keywords to verify that the search functionality works correctly.

Tests performed:

Search using keyword "mouse" returned the product Wireless Mouse.
Search using "MOUSE" returned the same result, confirming that the search is case-insensitive.
Search using the keyword "e" returned multiple products containing the letter "e".
Search using "laptop" returned a message indicating that no products were found.

This confirmed that the search endpoint works correctly with both matching and non-matching queries.

Question 2 – Product Sorting (GET)

Endpoint used:

GET /products/sort

The sorting API was tested with different query parameters.

Tests performed:

Sorting by price in ascending order returned products from cheapest to most expensive.
Sorting by price in descending order returned products from highest price to lowest price.
Sorting by name in alphabetical order arranged products from A to Z.
An invalid parameter sort_by=category was tested and the API returned an error message indicating that only price or name are allowed.

This verified that sorting works correctly and invalid inputs are handled properly.

Question 3 – Product Pagination (GET)

Endpoint used:

GET /products/page

Pagination was implemented using page and limit query parameters.

Tests performed:

Page 1 with limit 2 returned the first two products.
Page 2 with limit 2 returned the remaining products.
Page 3 with limit 2 returned an empty list because no more products were available.
Using limit 1 confirmed that the total number of pages increases accordingly.

This demonstrated how APIs can return large datasets in smaller paginated responses.

Question 4 – Search Orders by Customer Name (GET)

Endpoint used:

GET /orders/search

This endpoint allows searching orders using the customer name.

Tests performed:

Multiple orders were created using the POST /orders endpoint.
Searching using a customer name returned all matching orders.
If no orders matched the search query, the API returned a friendly message indicating that no orders were found.

This feature helps administrators quickly find orders placed by specific customers.

Question 5 – Sort Products by Category and Price (GET)

Endpoint used:

GET /products/sort-by-category

This endpoint sorts products in two levels:

First by category in alphabetical order.
Then by price in ascending order within each category.

This allows the store administrator to view products grouped by category while still maintaining price order inside each group.

Question 6 – Browse Products (Search + Sort + Pagination)

Endpoint used:

GET /products/browse

This endpoint combines multiple features into a single API.

Features implemented:

Keyword search for filtering products.
Sorting by price or name.
Pagination using page and limit parameters.

Tests performed:

Calling the endpoint without parameters returned all products sorted by price in ascending order.
Calling the endpoint with keyword, sorting, and pagination parameters returned filtered and paginated results.

This endpoint simulates real-world e-commerce browsing functionality.

Bonus – Orders Pagination (GET)

Endpoint used:

GET /orders/page

Pagination was implemented for the orders list.

Tests performed:

Multiple orders were created to generate enough data.
Page 1 and Page 2 returned different sets of orders.
The API correctly calculated the total number of pages.

This feature helps manage large order lists efficiently.

Tools Used

Python
FastAPI
Swagger UI
Uvicorn
