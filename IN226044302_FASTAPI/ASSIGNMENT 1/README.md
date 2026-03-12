# FastAPI Assignment 1 – Day 1

The objective of this assignment was to understand the basics of **FastAPI endpoints, path parameters, and API responses**.

# Question 1 – Add More Products

Three new products were added to the existing `products` list.

Products added:

1. Laptop Stand  
2. Mechanical Keyboard  
3. Webcam  

Each product includes the following fields:

- id  
- name  
- price  
- category  
- in_stock  

After adding the products, the `/products` endpoint returned **7 total products**.

---

# Question 2 – Category Filter Endpoint

A new endpoint was created:

GET /products/category/{category_name}

This endpoint returns products that belong to a specific category.

Example:

GET /products/category/Electronics

Output shows only products from the Electronics category.

If the category does not exist, the API returns:

{"error": "No products found in this category"}

---

# Question 3 – In-Stock Products Endpoint

Endpoint created:

GET /products/instock

This endpoint returns only products where:

in_stock = True

The response includes:

- list of available products
- total count of available products

---

# Question 4 – Store Summary Endpoint

Endpoint created:

GET /store/summary

This endpoint returns store statistics including:

- Store name
- Total number of products
- Number of products in stock
- Number of products out of stock
- List of available categories

This provides a quick overview of the store inventory.

---

# Question 5 – Search Products by Name

A search functionality was implemented to allow users to search products using a keyword.

Example:

GET /products/search?name=mouse

The endpoint returns all products whose name contains the given keyword.

---

# Tools Used

- Python
- FastAPI
- Swagger UI
- Uvicorn
