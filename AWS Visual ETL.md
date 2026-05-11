### Custom Transformation Example

![[Pasted image 20260509062535.png]]

in AWS Glue Studio Visual ETL, data is internally passed between nodes as **DynamicFrames / DynamicFrameCollections**, not standard Spark DataFrames by default.

DFC(A collection/group of multiple DynamicFrames)

| Type                   | Used In                              |
| ---------------------- | ------------------------------------ |
| DataFrame              | Native Spark                         |
| DynamicFrame           | AWS Glue abstraction                 |
| DynamicFrameCollection | Collection of multiple DynamicFrames |

In order to run SQL queries/Some Transformations  on such files the DFC usually need to transformed into regular DF(DataFrame) First.

```
def MyTransform (glueContext, dfc) -> DynamicFrameCollection:
        
    # Importing Functions
    from pyspark.sql.functions import col
    
    # Get the input DynamicFrame
    dyf = dfc.select(list(dfc.keys())[0])
    
    # Convert to DataFrame
    df = dyf.toDF()
    
    # Multiply two columns
    df = df.withColumn(
        "total_value",
        col("Price") * col("Quantity")
    )
    
    # Convert back to DynamicFrame
    result_dyf = DynamicFrame.fromDF(df, glueContext, "result_dyf")
    
    return DynamicFrameCollection({"result": result_dyf}, glueContext)
```
# Why Does Visual ETL Use It?

In visual pipelines:
- one node may output multiple datasets
- transformations may branch
- joins/splits create multiple outputs


# Whenever dealing with Big Data we like to keep our data Partitioned.

![[Pasted image 20260509064625.png|329]]

# DeltaLake does not allow 
```
' '  (space)
','  ';'  '{'  '}'
'('  ')'
'\n' '\t'
'='
```
as column names

