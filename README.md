# ECE-2112-PA3

Ricohermoso, Mary Loren P. | 2ECE-B

This repository contains the Programming Assignment 3 for "Advance Computer Programming" this A.Y. 2026-2027. This covers Pandas data analysis conceptss, specifically positional and label-data slicing, Boolean filtering, and multi-model subsetting using the dataset given. 

## A. POSITIONAL AND LABEL-BASED SLICING

  Load the `cars.csv ` dataset, display its dimensions and column names, then create a slice `cars_6_to_10 ` containing rows 6 through 10 with only the columns `Model `, `mpg`, `cyl`, `hp`, and `gear`.

These are the Functions that are used in this Problem:

`• pd.read_csv()` - A pandas function used to read a CSV data set into a DataFrame. 

Example: 

  `cars = pd.read_csv('cars.csv')`

`• .shape` - A DataFrame attribute returning a tuple representing dimensions (rows, columns).

Example:

  `cars.shape --> (32,12)`

`• .iloc()` - An intege-location based indexing method used to select rows by numerical position. To extract rows 6 through 10, index range `[5:10]` is used due to zero-based indexing. 

Example

  `cars.iloc[5:10]`

`• .loc()` - A label-based indexing method used to filter DataFrame columns by name.

Example: 

  `cars_6_to_10.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]`

Combining all these Functions, the code used for this is: 

  ```Phyton
import pandas as pd

cars = pd.read_csv('cars.csv')
cars

cars.shape

 















  
