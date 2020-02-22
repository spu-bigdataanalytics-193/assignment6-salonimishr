# assignment6-salonimishr
assignment6-salonimishr created by GitHub Classroom
In this bonus assignment, I used Databricks platform for creating a notebook where one can read a dataset, explore the dataset in various
ways. As I used Databricks community edition, it doesn't allow to configure Spark but in the notebook all options are given. For this
assignment, I used Amazon dataset Luxury_Beauty along with Magazine_Subscription. First I read the both datasets in dataframe and then 
converted Luxury_Beauty dataframe in rdd then changed it back again in the Pyspark dataframe. After this I changed Pyspark dataframe to 
Pandas Dataframe. But for further functions, I used pyspark dataframe. Before going further I checked the schema and counts of dataframe. Then 
I completed following tasks by using sql queries:
*Select first 10 rows of dataset.
*Shown the schema of of the dataset.
*Used Group by and got max, min, count of a column in the dataset.
*Filter the dataset.
*Applied order by.
*Applied inner join/ left join/ right join on two dataframes. For this purpose I used Magazine_subscription dataset and Luxury_Beauty.
*Selected distinct records by overall variable.
*Created an user defined function "say_hello" and used it in creating a new variable "greetings".In this variable UDF printed hello along 
with reviewerName.
*Transformed overall column with OneHot Encoding.

As having with Groupby is not supported in Spark so it is not here. In these dataset, there were no continuous variables.
