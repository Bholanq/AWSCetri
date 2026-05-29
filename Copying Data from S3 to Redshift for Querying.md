# COPY command 
```
CREATE TABLE customers (
    id INT,
    name VARCHAR(100),
    age INT
);

COPY customers
FROM 's3://my-data-bucket/sales/customers.csv'
IAM_ROLE 'arn:aws:iam::123456789012:role/MyRedshiftRole'
CSV
IGNOREHEADER 1;

SELECT * FROM customers;
```


- Uploaded .csv data to landing_layer.
