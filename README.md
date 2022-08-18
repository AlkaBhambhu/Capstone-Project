# Customer Behaviour and Market Basket Analysis
 
 Predictive analytics combines several statistical techniques such as data mining, predictive modeling, and machine learning to make predictions about future events based on historical data.
 
 This project focuses on the development of an end-to-end automated solution that helps predict which reordered products a user will buy again. 
 
 First, we perform the data analysis to understand the orders, then segment consumers based on buying behavior and explore the association between products, and at last deploy prediction models. 
 
 The sequential ensemble model derives an accuracy of 72.82% and a Recall score of 73.44%. The lift chart shows that taking the 30% of the records that are ranked by the model as “most probable reordered” yields 5 times as many reorder’s as would randomly selecting 30% of the records. 
 
 This model will help Instacart to send personalized push notifications, estimate the basket of the user, and pre-fill the cart with the products that the customer is most likely to buy. This framework will increase the value of the service by saving customers’ time and triggering new purchases through personalized push notifications.


# Project Deliverables 
- Introduction 
  - Background, Problem statment & Objective
- Data Exploration
- Customer Segmentation
- Association Rules
- Feature Engineering
- Predictive Models
- Model Governance 
- Presentation

## Data Dictionary:

### Initial Dataframe

| Feature          | Datatype | Description                                                                                                      |
|------------------|----------|------------------------------------------------------------------------------------------------------------------|
| `aisle_id`       | integer    | aisle identifer                                                                             |
| `aisle`          | string   | aisle                                                                                             |
| `product_id`     | integer  | Product identifer                                                                                       |
| `product_name`   | string    | name of the product|
| `department_id`  | integer  | Department identifer                                                                         |
| `department`     | string  | department name
| `order_id`       | integer  | Order identifer                                                                                        |
| `eval_set`       | string  | prior/train,  where "prior": orders prior to that users most recent order & "train": most recent orders                                                                               
| `order_number`   | integer  | Order sequence number                                                                                     |
| `order_dow`      | integer  | Hour of the day the order was placed                                           |
| `order_hour_of_the_day`  | integer    | Size by square feet                                                                                              |
| `days_since_prior` | integer | days since the last order, capped at 30

### Added Features

| Feature                   | Datatype       | Description                                                                                                      |
|---------------------------|----------------|------------------------------------------------------------------------------------------------------------------|
| `total_orders_per_user`   | integer    | Number of orders by a user|
| `total_products_per_user`   | integer    | Number of products bought by a user |
| `unique_products_per_user`  | integer | Number of unique products bought by a user | 
| `total_reorders_per_user` | float | Number of reordered products by a user |
| `reorder_ratio_per_user` | float | Average of reorders by a user |
| `avg_gap_in_orders_per_user` | float | Average number of days since prior order |
| `prod_reorder_ratio` | integer | Average reorders for a product |
| `num_orders_for_prod` | integer | Total number of orders for a product |
| `avg_cart_order_of_product` | float | Average sequence in which a product is added to the cart |
| `is_organic` | integer | 1 if a product is organic, else 0 |
| `is_vegan` | integer | 1 if a product is vegan, else 0| 
| `is_Gluten-free` | integer | 1 if a product is gluten-free, else 0 |
| `total_prod_by_user` |  integer | Number of orders per product by a user |
| `prod_reorder_by_user` | integer | Number of reorders per product by a user |
| `prod_reorder_ratio_by_user` | integer | Average reorders per product by a user |
| `days_since_prior_prod_user` | integer | Average days since prior order for a product by a user |

### Target
| Feature                   | Datatype       | Description                                                                                                      |
|---------------------------|----------------|------------------------------------------------------------------------------------------------------------------|
| `redordered`                | integer        | 1 if this product has been ordered by a user, 0 otherwise

---
