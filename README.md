# MongoDB Queries

## 1. Retrieve all information about each product:
    
    ```bash
    db.products.find({})

## 2. Find products with a price between 400 and 800:
    ```bash
    db.products.find({ "product_price": { $gte: 400, $lte: 800 } })
    
## 3. Find products with a price not between 400 and 600:
    ```bash
    db.products.find({ "product_price": { $not: { $gte: 400, $lte: 600 } } })

## 4. List the first four products with a price greater than 500:
    ```bash
    db.products.find({ "product_price": { $gt: 500 } }).limit(4)

## 5. Retrieve the product name and material of each product:
    ```bash
    db.products.find({}, { "product_name": 1, "product_material": 1, "_id": 0 })

## 6. Find the product with an ID of 10:
    ```bash 
    db.products.find({ "id": "10" })

## 7. Retrieve only the product name and material:
    ```bash 
    db.products.find({}, { "product_name": 1, "product_material": 1, "_id": 0 })

## 8. Find all products where the material is "Soft":
    ```bash 
    db.products.find({ "product_material": "Soft" })

## 9. Find products that are indigo in color and priced at 492.00:
    ```bash
    db.products.find({ "product_color": "indigo", "product_price": 492.00 })

## 10. Delete products with a price of 28:
    ```bash
    db.products.deleteMany({ "product_price": 28 })




