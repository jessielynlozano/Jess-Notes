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
