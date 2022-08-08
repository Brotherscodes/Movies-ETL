# Movies-Extract_Transform_Load

## Project Overview:

An Extract-Transform-Load pipeline was created to extract the three movie related databases provided and then loaded into a single SQL database. Data can come from many sources, but most needs to be cleaned and structured before any noteworthy analysis can be performed. Using Python and Pandas I explored the data and performed any neccessary data transformation to maintain its integrity and consistency. Lastly, the clean final data was loaded into a postgreSQL database.

<br />
<br />

<p align="center"> 
<image src="Images/E_T_L.png" width= "75%" height="75%"

<br />


## Outline: 

1. Write an ETL Function to Read Three Data Files
2. Extract and Transform the Wikipedia Data
3. Extract and Transform the Kaggle data
4. Create the Movie Database



#

<br />

### A file directory was created and used to read in the three data files. Variables were created for these files as seen below. Using the "with open" statement I read in the two CSV files as Pandas DataFrames and the json file in json format for better readability. Please reference the complete "ETL_create_database.ipynb" file in the Project_Files folder in this repositiory to see the completed ETL function I used to import the movie data and transform/parse the data.

<br />

<p align="center">
<image src="Images/loading_in_files.png" width="75%"

<br />

<p align="center">
<image src="Images/file_dir_and_variables.png" width="75%"

<br />

#

<br />

### Once the data was parsed and clean, the movies_df DataFrame and MovieLens ratings csv data were then loaded into a SQL database using postgreSQL and PgAdmin. A Database Engine was created to complete this task. My pgAdmin password was saved in a seperate config.py file and pulled in from this file with our dependencies. The data from our ratings.csv file consisted of over 26 million rows, therefore, I loaded this data in 1 million rows at a time and displayed the elapsed time.


<br />

<p align="center">
<image src="Images/create_database.png" width="80%"

<br />



<br />

<p align="center">
<image src="Images/import_data_time.png" width="70%"

<br />




<br />

#


<br />

### Once the movies_df DataFrame and MovieLens ratings csv data were successfully loaded into the SQL database, I tested the output to verify it was correct. The following queries were created. PNG files of these queries are also located in the Images Folder for reference. The complete code can be found in the "ETL_create_database.ipynb" file in the Project_Files folder.

<br />

<p align="center">
<image src="Images/movies_query.png" width="100%"

<br />

<br />

<p align="center">
<image src="Images/ratings_query.png" width="50%"

<br />

<br />

### The data we started with was cleaned by calling our single function we wrote defined as "extract_transform_load."

<br />

Resources:

- movies_metadata.csv
- ratings.csv
- wikipedia-movies.json
- Software: Jupyter Lab, Pandas, Python, JSON, PostgreSQL, PgAdmin,VS Code