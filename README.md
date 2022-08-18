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
| `aisle_id`       | int64    | aisle identifer                                                                             |
| `aisle`          | object   | aisle                                                                                             |
| `product_id`     | float64  | Product identifer                                                                                       |
| `product_name`   | int64    | name of the product|
| `department_id`  | float64  | Department identifer                                                                         |
| `department`     | object  | department name
| `order_id`       | float64  | Order identifer                                                                                        |
| `eval_set`       | float64  | prior/train                                                                                 |
| `order_number`   | float64  | Order sequence number                                                                                     |
| `order_dow`      | float64  | Hour of the day the order was placed                                           |
| `order_hour_of_the_day`  | int64    | Size by square feet                                                                                              |
| `days_since_prior` | int64 | days since the last order, capped at 30
