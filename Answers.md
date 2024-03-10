1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
    In the provided schema, the relationship between the "Product" and "Product_Category" entities is established through a foreign key constraint that is"category_id" column in the "Product" table serves as a foreign key referencing the primary key "id" 
    in the "Product_Category" table. This indicates that each product is associated with one category.

     One-to-Many Relationship: This relationship represents a one-to-many association where one product belongs to one category, but each category can have multiple products associated with it.
   
     Foreign Key Constraint:The foreign key constraint ensures referential integrity by guaranteeing that the value stored in the "category_id" column of the "Product" table must exist in the "id" column of the "Product_Category" table.

2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
   To ensure that each product in the "Product" table has a valid category assigned to it.

    Foreign Key Constraint: As mentioned earlier, the foreign key constraint on the "category_id" column in the "Product" table ensures that the value stored in this column must correspond to a valid category ID in the "Product_Category" table. This 
    prevents the insertion or update of a product with a non-existent category.

    Validation Rules: Additionally, we can implement validation rules at the application level to ensure that a product cannot be created or updated without specifying a valid category. This can include frontend validation checks or backend validation 
    logic before persisting data to the database.
