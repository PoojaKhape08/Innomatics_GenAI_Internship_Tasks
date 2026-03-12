# FastAPI Assignment 2 – Day 2

The objective of this assignment was to practice **Query Parameters, GET APIs, POST APIs, and Pydantic validation** using FastAPI.

# Question 1 – Minimum Price Filter

The existing endpoint `/products/filter` was extended with a new query parameter:

min_price

Example:

GET /products/filter?min_price=400

This returns only products with price greater than or equal to the given value.

The filter works together with other filters like:

- category
- max_price
- in_stock

---

# Question 2 – Product Price Endpoint

A new endpoint was created:

GET /products/{product_id}/price

This endpoint returns only:

- product name
- product price

Example response:

{
"name": "Wireless Mouse",
"price": 499
}

If the product does not exist, the API returns:

{"error": "Product not found"}

---

# Question 3 – Customer Feedback API

A Pydantic model **CustomerFeedback** was created with fields:

- customer_name
- product_id
- rating
- comment

Endpoint created:

POST /feedback

This endpoint:

- accepts feedback data
- validates rating between 1 and 5
- saves feedback into a list

Response includes the submitted feedback and total feedback count.

---

# Question 4 – Product Summary Dashboard

Endpoint created:

GET /products/summary

This endpoint returns store analytics including:

- total products
- in stock count
- out of stock count
- most expensive product
- cheapest product
- available categories

This endpoint acts as a quick **dashboard for store inventory**.

---

# Question 5 – Bulk Order Validation

A POST API was implemented to place bulk orders with proper validation using Pydantic models.

The endpoint validates:

- product availability
- order quantity
- product ID validity

This ensures correct order processing.

---

# Tools Used

- Python
- FastAPI
- Swagger UI
- Uvicorn
