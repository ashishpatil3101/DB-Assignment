### Quesion 1)  Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

- ans = > The relationship between the "Product" and "Product_Category" entities is established through a structured association in the database schema. This association is characterized by a one-to-many relationship, wherein each record in the "Product" entity is  linked to a specific category represented in the "Product_Category" entity. The relational linkage is can be find  through the utilization of a foreign key, namely category_id in the "Product" entity, which references the primary key id in the "Product_Category" entity.
Also , this one-to-many relationship signifies that each individual product within the "Product" entity is affiliated with a singular category from the "Product_Category" entity. Conversely, each category within the "Product_Category" entity has the capacity to be associated with multiple products.



### Quesion 2)  How could you ensure that each product in the "Product" table has a valid category assigned to it? 

- ans = >To make sure each product in the "Product" table has a valid category, we use a system that checks and ensures that every category assigned to a product actually exists. We do this by setting up a rule that links the "Product" table to the "Product_Category" table. This rule, known as a foreign key constraint, prevents us from adding or updating a product with a category that isn't listed in the "Product_Category" table.

- In simpler terms, it's like having a checklist for categories, and each product can only be associated with a category that is on that checklist. This helps avoid mistakes and keeps our data organized and accurate. If someone tries to add a product with a category not on the list, the system won't allow it, ensuring that every product has a valid and recognized category.

- we can also do  this at Application-Level Validation
 Instead of relying on database-level constraints, you could implement validation checks within the application code that interacts with the database.
When adding or updating a product, the application code can perform a check to ensure that the specified category is valid by querying the "Product_Category" table