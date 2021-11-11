# Movies-ETL
Module 8 - ETL

#### Deliverable 1

- [x] 1. An ETL function is written to read in the three data files
- [x] 2. The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file
- [x] 3. The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file
- [x] 4. The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file

<kbd>
  <img src="https://github.com/GabrielaTuma/Movies-ETL/blob/f26922965b4b3541d5476530842b2e1e637458df/Resources/function_test%20ratings%20.png">
</kbd>  &nbsp;
</p>

[ETL_function_test.ipynb file](https://github.com/GabrielaTuma/Movies-ETL/blob/f26922965b4b3541d5476530842b2e1e637458df/ETL_function_test.ipynb)


#### Deliverable 2

- [x] 1. The TV shows are filtered out, and the wiki_movies_df DataFrame is created
- [x] 2. A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs

The extraction and transformation of the Wikipedia data in the ETL function does the following:
- [x] 3. A list comprehension is used to keep columns with non-null values
- [x] 4. The non-null box office data is converted to string values using the lambda and join functions
- [x] 5. A regular expression is used to match the six elements of "form_one" of the box office data
- [x] 6. A regular expression is used to match the three elements of "form_two" of the box office data
- [x] 7. The following columns are cleaned in the Wikipedia DataFrame:
- The box office column
- The budget column
- The release date column
- The running time column
- [x] 8. The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file

<kbd>
  <img src="https://github.com/GabrielaTuma/Movies-ETL/blob/f26922965b4b3541d5476530842b2e1e637458df/Resources/clean_wiki_movies%20columns%20.png">
</kbd>  &nbsp;
</p>

[ETL_clean_wiki_movies.ipynb file](https://github.com/GabrielaTuma/Movies-ETL/blob/f26922965b4b3541d5476530842b2e1e637458df/ETL_clean_wiki_movies.ipynb)


#### Deliverable 3

- [x] 1. The Kaggle metadata is cleaned
- [x] 2. The Wikipedia and Kaggle DataFrames are merged

- [x] 3. The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df:
- Unnecessary columns are dropped
- A function is used to fill in the missing Kaggle data
- The movies_df DataFrame is filtered to keep specific columns
- The movies_df DataFrame columns are renamed

- [x] 4. The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
- The ratings counts are cleaned
- The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame
- The empty values in the movies_with_ratings_df DataFrame are filled with “0”

- [x] 5. The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file


[ETL_clean_kaggle_data.ipynb file](https://github.com/GabrielaTuma/Movies-ETL/blob/f26922965b4b3541d5476530842b2e1e637458df/ETL_clean_kaggle_data.ipynb)




#### Deliverable 4

- [x] 1. The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png

<kbd>
  <img src="https://github.com/GabrielaTuma/Movies-ETL/blob/d8d83a9d3e110ba7fd7ad90efb711c4dcc9c68ec/Resources/movies_query.png">
</kbd>  &nbsp;
</p>

- [x] 2. The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png

<kbd>
  <img src="https://github.com/GabrielaTuma/Movies-ETL/blob/d8d83a9d3e110ba7fd7ad90efb711c4dcc9c68ec/Resources/ratings_query.png">
</kbd>  &nbsp;
</p>

- [x] 3. The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file

[ETL_create_database.ipynb file](https://github.com/GabrielaTuma/Movies-ETL/blob/f26922965b4b3541d5476530842b2e1e637458df/ETL_create_database.ipynb)



## Resources

- Software: Python 3.7.6, Visual Studio Code 1.58.1, Jupyter Notebook 6.3.0, pgAdmin 4 version 5.5
