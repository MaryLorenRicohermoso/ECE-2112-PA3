# ECE-2112-PA3

Ricohermoso, Mary Loren P. | 2ECE-B

This repository contains the Programming Assignment 3 for "Advance Computer Programming" this A.Y. 2026-2027. This covers Pandas data analysis concepts, specifically positional and label-data slicing, Boolean filtering, and multi-model subsetting using the dataset given. 

## *A. POSITIONAL AND LABEL-BASED SLICING*

  Load the `cars.csv ` dataset, display its dimensions and column names, then create a slice `cars_6_to_10 ` containing rows 6 through 10 with only the columns `Model `, `mpg`, `cyl`, `hp`, and `gear`.

These are the Functions that are used in this Problem:

• `pd.read_csv()` - A pandas function used to read a CSV data set into a DataFrame. 

Example: 

          cars = pd.read_csv('cars.csv')

• `.shape` - A DataFrame attribute returning a tuple representing dimensions (rows, columns).

Example:

          cars.shape --> (32,12)

• `.iloc()` - An intege-location based indexing method used to select rows by numerical position. To extract rows 6 through 10, index range `[5:10]` is used due to zero-based indexing. 

Example

          cars.iloc[5:10]

• `.loc()` - A label-based indexing method used to filter DataFrame columns by name.

Example: 

            cars_6_to_10.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]

Combining all these Functions, the code used for this is: 

```Python

import pandas as pd

cars = pd.read_csv('cars.csv')
cars

cars.shape

cars_6_to_10 = cars.iloc [5:10]
cars_6_to_10

cars_6_to_10 = cars_6_to_10.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]
cars_6_to_10

```

## *B. Model Lookup*

  Use Boolean indexing on the `Model` column to look op specific vehicles without row numbers.
  
   *Find the complete row for `'Toyota Corolla', 'Pontiac Firebird'`.
                  
   *Displaying only `'Model', 'mpg', 'hp', 'wt'`.

These are the Functions that are used in this Problem:

• `cars['Model'] == '.....' (Boolean Indexing)` - Compares column values against a target string to generate a True/False mask for matching rows. 

Example:   

            cars['Model'] == 'Toyota Corolla'

• `.loc[condition, columns]` - Filters rows where the condition evaluates to `True` while specifying desired column labels. 

Example:

            cars.loc[cars['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]

Combining all these Functions, the code used for this is:

```Python
import pandas as pd

toyota = cars.loc[cars ['Model'] == 'Toyota Corolla']
toyota

pontiac = cars.loc[cars ['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]
pontiac
```

## C. Multi-Model Subsetting

  Extract records for `"Datsun 710", "Lotus Europa", and "Ferrari Dino"` into a new DataFrame named `selected_cars`, retaining only column `'Models', 'mpg', 'cyl', 'hp', and 'gear'`. Confirm that the final DataFrame contains 3 rows and 5 columns. 

These are the Functions that are used in this Problem:

• `.isin()` - Checks whether elements in a Pandas Series match any values provided in a list. 

Example:

        cars['Model'].isin(['Datsun 710', 'Lotus Europa', 'Ferrari Dino']) 

• `.shape()` - Used to confirm the resulting subset.

Example: 
    
        selected_cars.shape ---> (3,5)


Combining all these Functions, the code used for this is:

```Python

import pandas as pd

selected_cars = cars.loc[cars['Model'].isin(['Datsun 710', 'Lotus Europa', 'Ferrari Dino'])

selected_cars = selected_cars.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]
selected_cars

selected_cars.shape

```

## Thank you for reading!

To see the main python program for Programming Assignment 3, click this link https://github.com/MaryLorenRicohermoso/ECE-2112-PA3/blob/main/Ricohermoso_2ECEB_PA3.ipynb  and download. Open on Jupyter Notebook, then run all cells.

# README file Version History:
September 6, 2026 - Initial README output uploaded







  
