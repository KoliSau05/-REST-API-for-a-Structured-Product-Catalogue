# -REST-API-for-a-Structured-Product-Catalogue
RESTful API for a product catalogue system is  utilizing Java and MySQL to store and manage products with a complex, nested data structure.

Features
Create Product: Add new products to the catalogue.
Read Product: Retrieve product details including name, description, price, categories, attributes, availability, and user ratings.
Update Product: Modify existing product information.
Delete Product: Remove products from the catalogue.
Search Products: Search for products based on various criteria such as name, category, price range, etc.
Pagination and Sorting: Implement pagination and sorting in the product list retrieval endpoint
User Ratings: Allow users to rate products and leave optional comments.
Product Entity Structure
Create Product: Add new products to the catalogue.
name: The name of the product.
description: A text description of the product.
price: The price of the product.
categories: An array of categories (strings) the product belongs to.
attributes: An array of key-value pairs (objects) for additional attributes such as size, color, brand, etc.
availability: An object containing:
inStock: A boolean indicating if the product is in stock.
quantity: An integer representing the available quantity.
ratings: An array of objects representing user ratings, each with:
userId: A unique identifier for the user who gave the rating.
rating: A numerical rating value.
comment: An optional text comment on the rating.
Technologies Used
Java
Spring Boot
Hibernate(ORM)
MySql
Installation
Clone the repository.
Install dependencies.
Configure MySql connection(Hibernate(ORM))
Run the application.
Usage
Start the application.
Access the API endpoints using a tool Postman.
Running Tests
To run tests on Postman

http://localhost:8090/api/allproducts
Retrieve all product details on data

  {
   "id": 1,
        "name": "Red Dress",
        "description": "A beautiful red dress for special occasions",
        "price": 39.99,
        "categories": "Clothing",
        "attributes": "Color: Red, Size: Medium",
        "availability": {
            "id": 1,
            "inStock": true,
            "quantity": 10 } 
    }
  {
    "id": 2,
    "name": "Kitchen Knife Set",
    "description": "Essential knives for every kitchen",
    "price": 49.99,
    "categories": "Kitchenware",
    "attributes": "Set of 5 knives with wooden handles",
    "availability": {
        "id": 3,
        "inStock": true,
        "quantity": 20 } 
    }
   {
    "id": 3,
    "name": "Running Shoes",
    "description": "Comfortable shoes designed for running",
    "price": 79.99,
    "categories": "Footwear",
    "attributes": "Color: Black, Size: 9, Type: Running",
    "availability": {
        "id": 2,
        "inStock": false,
        "quantity": 0   }  
         } 
http://localhost:8099/api/allproducts/sort/price
sort the data according to thinks

 [
    {
        "id": 7,
        "name": "remote Name",
        "description": "Product Description",
        "price": 9.99,
        "categories": null,
        "attributes": null,
        "availability": null,
        "ratings": []
    },
    {
        "id": 4,
        "name": "Example Product",
        "description": "This is an example product description.",
        "price": 19.99,
        "categories": "Electronics, Gadgets",
        "attributes": "{\"color\": \"red\", \"size\": \"large\", \"weight\": \"1kg\"}",
        "availability": null,
        "ratings": []
    },
    {
        "id": 6,
        "name": "smart Product",
        "description": "This is an example product description.",
        "price": 19.99,
        "categories": "Electronics, Gadgets",
        "attributes": "{\"color\": \"red\", \"size\": \"large\", \"weight\": \"1kg\"}",
        "availability": null,
        "ratings": []
    },
    {
        "id": 1,
        "name": "Red Dress",
        "description": "A beautiful red dress for special occasions",
        "price": 39.99,
        "categories": "Clothing",
        "attributes": "Color: Red, Size: Medium",
http://localhost:8099/api/pagination/0/3
 {
    "content": [
        {
            "id": 1,
            "name": "Red Dress",
            "description": "A beautiful red dress for special occasions",
            "price": 39.99,
            "categories": "Clothing",
            "attributes": "Color: Red, Size: Medium",
            "availability": {
                "id": 1,
                "inStock": true,
                "quantity": 10}
  {
    "id": 2,
    "name": "Kitchen Knife Set",
    "description": "Essential knives for every kitchen",
    "price": 49.99,
    "categories": "Kitchenware",
    "attributes": "Set of 5 knives with wooden handles",
    "availability": {
        "id": 3,
        "inStock": true,
        "quantity": 20}}]}
update product..http://localhost:8085/api/product/update/5.

delete product..http://localhost:8086/product/delete/1

create rating..http://localhost:8088/rating/add

retrive rating http://localhost:8088/rating

delete rating... http://localhost:8088/deleteRating/3

create availability..http://localhost:8088/addavailability

delete availability...http://localhost:8088/deleteAvailability/5

get availability...http://localhost:8088/addavailability

Contributors
Saurabh Koli
Project Link :- (https://github.com/KoliSau05/-REST-API-for-a-Structured-Product-Catalogue/tree/productcatalogue/SainugenAces_PLTT_SainugenAces_PLTT)
