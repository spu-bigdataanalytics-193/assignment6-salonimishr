# Spark Even More! (Bonus)

![Spark API](https://databricks.com/wp-content/uploads/2016/06/Unified-Apache-Spark-2.0-API-1.png)
In this assignment, you will implement various ways of using Spark. The goal in this assignment is to use functionalities of spark.

**PS: This assignment is not mandatory if you think you collected enough points. If not this may be your chance to increase your points!**

Hint: All the answers of the tasks given below, you can find it right in the [Spark Python Documentation](https://spark.apache.org/docs/latest/api/python/index.html).

## Dataset

You can use the [Amazon Product Review Dataset](https://nijianmo.github.io/amazon/index.html) with the whole dataset or the smallest one, or any other dataset that you feel comfortable with. You may need two datasets at least to be able to perform some operations, such as joins.

For amazon product review dataset, review and the metadata datasets could be your two datasets. 

You can use small and simple datasets, you can create the dataset on your own, since some of the tasks may require multiple datasets.

## Assignment Instructions

Here in this assignment, the goal is to create a notebook where you read a dataset, explore the dataset in various ways, extract some statistics, and showcase your results.

There will be following headings.

1. Explore configuration options on SparkSession 
2. Reading the data
3. Performing Tasks
    - Exploring the data with Spark SQL
    - Exploring the data with Spark DataFrame


In your notebook, you need a heading for each of these 4 categories.

Under each category, you need to show the description for the task and the code together.

For the 3rd task, you can create a subheading for each task and show both versions of your code under one description. Following is the illustration of how your notebooks should be.

``` md
...

## Reading Data

Your description of the code below.

    `# your spark code to read dataframe`

## Performing Tasks

### Task 1 - Get Schema of Dataset

...

### Task 2 - Select first N Rows

Selecting rows with sql query.

    `sparkSession.sql(`select top 10 from dataset`).collect()`

Selecting rows with pyspark.sql.DataFrame API.

    `select().take(10)`

### Task 2 - Apply order by

Your lengty description of what your code does.

...

```

### 1. Explore Spark configuration options

Find **at least 5** different option of spark and initiate your spark session based on these options.

``` py
SparkSession.builder.config("spark.some.config.option", "some-value")
```

### 2. Reading the data

Read your dataset from a file, and from a table. You can upload your data to `DataBricks` as a table in order to do table operations. 

``` py
spark.read.csv(...)
```

From the list below, do **all** of the operations.

- Read data as RDD
- Read data as DataFrame
- Convert RDD to Spark DataFrame
- Convert Spark DataFrame to RDD
- Convert Spark DataFrame to Pandas DataFrame

### 3. Tasks

From following tasks, you need to do **at least 8** of them to get the full points in both ways, by writing SQL queries and by using pyspark.sql.DataFrame functions. You **must show the result**  of your task by showing first few rows of your dataset, if not the rows, similarly, the aggreated result from your code.

- Select first 10 rows of dataset.
- Show the schema of of the dataset.
- Group by and get max, min, count of a column in the dataset.
- Filter your dataset by some conditions based on your column.
- Apply group by with having clause.
- Apply order by.
- Apply inner join/ left join/ right join on your two tables.
- Select distinct records by a column.
- Register a user defined function to Spark and use it in your Spark SQL Query.
- Transform the data type of columns from int to string/ string to integer.
- Apply a min-max normalization on any numerical column.
- Apply a standard normalization on any numerical column.
- Transform a categorical column with OneHot Encoding.
- Use Spark.sql.DataFrameStatFunctions to collect statistics from the data. 
    - Get covariance
    - Get correlation
    - Get crosstab
    - Get freqItems


#### Spark SQL

To do the tasks with Spark SQL, you need to implement the tasks by writing SQL queries and executing your results with Spark SQL.

``` py
your_query = 'select * from tablename'
sparkSession.sql(your_query).show()
```

#### Spark DataFrame

To do the tasks with Spark DataFrame, you need to use pyspark.sql.DataFrame functions like below.

``` py
data.select(...).groupBy(...)
```

## What are all these other files?

Following table is will give it a meaning for each file.

File                | Description 
-------             | ----------- 
README.md **        | A descriptive file to give an introduction of current project/ assignment. 
Instructions.md **  | A copy of current README.md file. 
LICENCE **          | The licence of the file that every project should have.
.gitignore          | The file to control which files should be ignored by Git.
*.ipynb             | Assignment notebook with your Spark code. 
