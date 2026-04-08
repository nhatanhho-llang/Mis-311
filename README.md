# Mis-311 Part 1: Data Analysis and Insight
Data Overview
Source of Data: The dataset comes from the 10_Supermarket Sale.xlsx file, specifically the sales sheet. Each row represents a single customer transaction.
Size of Dataset:

Rows: 250 transactions
Columns: 10 variables
Variables:

sale_id: Unique identifier for each transaction
branch: Branch code (A or B)

city: City where the branch is located (New York, Los Angeles, Chicago)

customer_type: Type of customer (Member or Normal)

product_name: Specific product purchased (Apple, Shampoo, Notebook, Orange Juice, Detergent)

product_category: Broader product category (Fruits, Personal Care, Stationery, Household, Beverages)

quantity: Number of items purchased

total_price: Total value of the transaction

Price per unit: Unit price of the product purchased

Context:
This dataset captures detailed supermarket sales across multiple branches and cities. It allows analysis of customer behavior (Member vs Normal), product performance (by category and name), and financial outcomes (quantity, total price, unit price). The data is suitable for exploratory analysis to identify spending patterns, product trends, and branch performance.

Data Cleaning

a. Missing Values
Handling Missing Values
Customer_type:

These are categorical variables → filled with the mode (most frequent value).

Product_category:

 Missing values in the product_category column were not filled using the most frequent value, as this would ignore the logical relationship between products and their categories. Instead, product categories were inferred based on the corresponding product_name, ensuring that each product was assigned to its correct and consistent category. This approach preserves the semantic accuracy of the dataset and improves the reliability of further analysis.

quantity:
 This is numerical → filled with the median quantity (11) to avoid distortion by extreme values.
 
b. Duplicate Rows

Duplicate rows found: 3

These rows were removed to avoid double-counting sales and inflating revenue or quantities.

Descriptive Statistics

Summary of Numerical Variables

<img width="538" height="291" alt="image" src="https://github.com/user-attachments/assets/294803f6-b3fe-47f4-aec7-c61c27a71464" />

Quantity:

The average number of items per transaction is 10.6, and the median is 11, which means the distribution is fairly balanced. However, the most frequent value (mode) is 2, showing that many customers often buy just a small number of items. The standard deviation of 5.99 indicates moderate variability, with transactions ranging from very small to quite large.
Total Price:

The average total price per transaction is about 124.2, while the median is lower at 95.43, suggesting that a few very high‑value transactions are pulling the average upward. The most common transaction value (mode) is 212.82, which appears frequently in the dataset. The standard deviation of 102.98 is quite high, reflecting significant differences in transaction sizes.

<img width="255" height="287" alt="image" src="https://github.com/user-attachments/assets/8ccb3587-ea3a-42fd-8113-598eb008544b" />

Price per Unit:
The average unit price is 11.62, and the median is 11.46, which are very close, indicating a stable and balanced distribution of product prices. There is no clear mode, meaning no single price dominates the dataset. The standard deviation of 6.12 shows moderate variation, reflecting the mix of low‑priced and higher‑priced products.

VISUALIZATION

<img width="752" height="452" alt="image" src="https://github.com/user-attachments/assets/a74412d0-d5ee-4f81-b0e9-96d54529f206" />

Insight 1: Members spend more than normal customers Based on the statistics, transactions from Members generally have higher average total_price and Revenue compared to Normal customers. This indicates that the membership program is effective in driving spending, suggesting that the supermarket should continue to strengthen and expand its loyalty policies.

<img width="752" height="452" alt="image" src="https://github.com/user-attachments/assets/b10cc9d8-01ed-4190-b128-4e91342e098f" />

<img width="752" height="452" alt="image" src="https://github.com/user-attachments/assets/2c1f7d87-ae7c-44e9-85f3-9b519b74f17b" />

Insight 2: The bar charts reveal that Shampoo and Notebook are the top-performing products in terms of both units sold and total sales value. Shampoo leads in quantity with over 600 units sold and also generates the highest revenue, indicating strong and consistent demand. Notebook follows closely, showing high transaction frequency and substantial contribution to overall sales.
This dual dominance suggests that Personal Care and Stationery categories are strategic revenue drivers. The supermarket should prioritize these products in inventory planning, promotional campaigns, and customer engagement strategies to maximize profitability and customer satisfaction.
