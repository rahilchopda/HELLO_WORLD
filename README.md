
# Data Loading

Performing data loading in Python and exporting the sales pre and post 2005 into a distinct .csv file in SQL. 


## Getting Started
These instructions will enable you to obtain and activate a duplicate of the project on your personal computer for the purpose of development and testing.   Refer to the deployment section for instructions on how to implement the project on a live system. 

## Prerequisites 
The following prerequisites are necessary to execute this code in Python: 

Install Anaconda. 
Configure Jupiter notebook. 
Configure MySQL. 
Generate a fresh userid and password in MySQL. 


## Installing
Jupiter notebook from Anaconda works with Python. We will then install Python libraries to communicate with MYSQL and conduct SQL queries. Next, we'll import Pandas, which converts tables into dataframes and does other operations. To interact with MYSQL, we'll import pymysql.

## Running the tests
To start, we made a pandas dataframe and read the vgsales.csv file into it. 
Then we use the df.head() function to show the rows and columns and the df.info() function to find out what kind of dataset it is.
Then, iloc is used to pick rows and columns from a DataFrame or Series based on where they are in the array instead of what they are named.
results_table is used to get the dataframe's return value.
Then we use top_1000 and df.iloc to choose rows from point 0 (inclusive) to 1000 (exclusive). This means we choose the first 1000 rows of the 4000 rows in the DataFrame.
Lastly, the create_engine method is used to make a database engine that connects to the MySQL database that was given.


## Breakdown of end to end steps

Create a pandas dataframe to read the vgsales.csv file. 
Using df.info(), we display all dataframe information. 
The df.info() function displays Columns, Column number, data kinds (integer, object, etc.), and if any Columns have values or null values. Also shown is dataframe memory use.
We enter a command to display the dataframe's rows and columns, revealing its shape.
Df.head() displays the top five dataframe rows.


#### Calculating the distribution of Channel type
Channeltype() calculates channel type distribution. This function accepts ‘data’. The iloc technique selects the first 1000 dataframe records.

Python's "integer location" technique selects data by integer indexing. It often works with Pandas DataFrames. Iloc lets you choose rows and columns from a DataFrame or Series by integer location rather than label. Distribution calculates the selected subset's 'channeltype' frequency distribution. Also, it is converted to percentages so users may see counts and percentages. The output has three columns: Channel Type, Count, and Percentage.

Function result_table returns the constructed DataFrame. With a DataFrame, this method returns a summary table of 'channeltype' values, counts, and percentages in the first 1000 rows of the incoming data.

dis displays the values of the top 1000 rows of the dataframe.

#### Filling a CSV file and database table with the top 1000 records
We chose the first 1000 rows of the DataFrame's 4000 rows using top_1000 and df.iloc.
Then we save the dataframe as CSV.
This code saves the DataFrame top_1000 to "top_1000_channels.csv" in the current working directory. This CSV file can be analyzed, shared, or fed into other programs. Pandas does not write row names (index) to the CSV file when set to False. If you remove this parameter or set it to True (the default), the CSV file's first column will be row names.

The result's row and column count is shown subsequently.


####MySQL server connection
Our connection URL includes the database type, username, password, host, and name. The create_engine function created a database engine to connect to the MySQL database. You can use the engine to access the database.

•'mysql+pymysql' specifies MySQL database dialect and Python MySQL driver.
•Calling database con=engine connects us to the database.

Following these procedures, we may load the CSV file into a MySQL database. 

## Deployment
There was no real-time deployment of this project. This project was a test to run a code for school. 
## Contributing

Contributions are always welcome! 

The following members contributed to this project:
PANKAJ
PARTH
JOHNSON


Please adhere to this project's `code of conduct`.


## Authors

RAHIL CHOPDA
Professor Omar Altrad
## License

License to use by Durham College


## Acknowledgements

Prof. Omar Altrad

PANKAJ SHARMA 
RAHIL CHOPDA
