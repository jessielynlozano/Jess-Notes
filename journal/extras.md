Cleaning using Mart
```sql
DROP TABLE IF EXISTS clean.grp12_4_instacart_orders;

CREATE TABLE clean.grp12_4_instacart_orders
(
  order_id                Nullable(Int32),
  user_id                 Nullable(Int32),
  eval_set                Nullable(String),
  order_number            Nullable(Int32),
  order_dow               Nullable(Int32),
  order_hour_of_day       Nullable(Int32),
  days_since_prior_order  Nullable(Float64)
)
ENGINE = MergeTree()
ORDER BY (ifNull(user_id, -1));

INSERT INTO clean.grp12_4_instacart_orders
SELECT
  CAST(order_id AS Nullable(Int32)),
  CAST(user_id AS Nullable(Int32)),
  CAST(eval_set AS Nullable(String)),
  CAST(order_number AS Nullable(Int32)),
  CAST(order_dow AS Nullable(Int32)),
  CAST(order_hour_of_day AS Nullable(Int32)),
  CAST(days_since_prior_order AS Nullable(Float64))
FROM raw.raw___insta_orders;
```

Instacart_Data Check: Ongoing
```sql
CREATE TABLE mart.grp4_2_instacart_raw_vs_clean
ENGINE = MergeTree()
ORDER BY tuple()
AS
SELECT
    (SELECT count(*) FROM raw.raw___insta_aisles) AS raw_aisles,
    (SELECT count(*) FROM clean.`2.4grp_instacart_aisles`) AS clean_aisles,
    (SELECT count(*) FROM raw.raw___insta_departments) AS raw_departments,
    (SELECT count(*) FROM clean.`2.4grp_instacart_departments`) AS clean_departments,
    (SELECT count(*) FROM raw.raw___insta_order_products_prior) AS raw_order_products_prior,
    (SELECT count(*) FROM clean.`2.4grp_instacart_order_products`) AS clean_order_products,
    (SELECT count(*) FROM raw.raw___insta_order_products_train) AS raw_order_products_train,
    (SELECT count(*) FROM clean.`2.4grp_instacart_order_products1`) AS clean_order_products_train,
    (SELECT count(*) FROM raw.raw___insta_orders) AS raw_orders,
    (SELECT count(*) FROM clean.`2.4grp_instacart_orders`) AS clean_orders,
    (SELECT count(*) FROM raw.raw___insta_products) AS raw_products,
    (SELECT count(*) FROM clean.`2.4grp_instacart_products`) AS clean_products;



-- 1. DROP the table if it exists to allow for rerunning the analysis
DROP TABLE IF EXISTS mart.grp4_2_instacart_null_analysis_fact_orders;

-- 2. CREATE a new table using the results of the UNION ALL query
CREATE TABLE mart.grp4_2_instacart_null_analysis_fact_orders 
ENGINE = MergeTree()
ORDER BY tuple()
AS
SELECT 
    mart.`2.4grp_instacart_fact_orders` AS source_table,
    'order_id' AS column_name,
    (CAST(SUM(CASE WHEN order_id IS NULL THEN 1 ELSE 0 END) AS REAL) * 100.0) / COUNT(*) AS null_percentage
FROM 
    mart.`2.4grp_instacart_fact_orders`

UNION ALL

SELECT 
    mart.`2.4grp_instacart_fact_orders` AS source_table,
    'user_id' AS column_name,
    (CAST(SUM(CASE WHEN user_id IS NULL THEN 1 ELSE 0 END) AS REAL) * 100.0) / COUNT(*) AS null_percentage
FROM 
    mart.`2.4grp_instacart_fact_orders`

UNION ALL

SELECT 
    mart.`2.4grp_instacart_fact_orders` AS source_table,
    'time_id' AS column_name,
    (CAST(SUM(CASE WHEN time_id IS NULL THEN 1 ELSE 0 END) AS REAL) * 100.0) / COUNT(*) AS null_percentage
FROM 
    mart.`2.4grp_instacart_fact_orders`

UNION ALL

SELECT 
    mart.`2.4grp_instacart_fact_orders` AS source_table,
    'order_number' AS column_name,
    (CAST(SUM(CASE WHEN order_number IS NULL THEN 1 ELSE 0 END) AS REAL) * 100.0) / COUNT(*) AS null_percentage
FROM 
    mart.`2.4grp_instacart_fact_orders`

UNION ALL

SELECT 
    mart.`2.4grp_instacart_fact_orders` AS source_table,
    'days_since_prior_order' AS column_name,
    (CAST(SUM(CASE WHEN days_since_prior_order IS NULL THEN 1 ELSE 0 END) AS REAL) * 100.0) / COUNT(*) AS null_percentage
FROM 
   mart.`2.4grp_instacart_fact_orders`;

-- 3. SELECT the new table to view the results (optional check)
SELECT * FROM mart.grp4_2_instacart_null_analysis_fact_orders
ORDER BY null_percentage DESC;
```
