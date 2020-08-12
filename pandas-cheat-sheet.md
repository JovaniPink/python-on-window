# Cheat Sheet

## DataFrame

> class pandas.DataFrame(data=None, index=None, columns=None, dtype=None, copy=False)
> Two-dimensional, size-mutable, potentially heterogeneous tabular data.

> Data structure also contains labeled axes (rows and columns). Arithmetic operations align on both row and column labels. Can be thought of as a dict-like container for Series objects. The primary pandas data structure.

### DataFrame Methods

|         FUNCTION          |                                                                                                           DESCRIPTION                                                                                                            |
| :-----------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|          index()          |                                                                                        Method returns index (row labels) of the DataFrame                                                                                        |
|         insert()          |                                                                                             Method inserts a column into a DataFrame                                                                                             |
|           add()           |                                                                        Method returns addition of dataframe and other, element-wise (binary operator add)                                                                        |
|           sub()           |                                                                      Method returns subtraction of dataframe and other, element-wise (binary operator sub)                                                                       |
|           mul()           |                                                                     Method returns multiplication of dataframe and other, element-wise (binary operator mul)                                                                     |
|           div()           |                                                                 Method returns floating division of dataframe and other, element-wise (binary operator truediv)                                                                  |
|         unique()          |                                                                                        Method extracts the unique values in the dataframe                                                                                        |
|         nunique()         |                                                                                    Method returns count of the unique values in the dataframe                                                                                    |
|      value_counts()       |                                                                           Method counts the number of times each unique value occurs within the Series                                                                           |
|         columns()         |                                                                                        Method returns the column labels of the DataFrame                                                                                         |
|          axes()           |                                                                                   Method returns a list representing the axes of the DataFrame                                                                                   |
|         isnull()          |                                                                               Method creates a Boolean Series for extracting rows with null values                                                                               |
|         notnull()         |                                                                             Method creates a Boolean Series for extracting rows with non-null values                                                                             |
|         between()         |                                                                          Method extracts rows where a column value falls in between a predefined range                                                                           |
|          isin()           |                                                                   Method extracts rows from a DataFrame where a column value exists in a predefined collection                                                                   |
|         dtypes()          |                                                        Method returns a Series with the data type of each column. The result’s index is the original DataFrame’s columns                                                         |
|         astype()          |                                                                                            Method converts the data types in a Series                                                                                            |
|         values()          |                                          Method returns a Numpy representation of the DataFrame i.e. only the values in the DataFrame will be returned, the axes labels will be removed                                          |
| sort_values()- Set1, Set2 |                                                                           Method sorts a data frame in Ascending or Descending order of passed Column                                                                            |
|       sort_index()        | Method sorts the values in a DataFrame based on their index positions or labels instead of their values but sometimes a data frame is made out of two or more data frames and hence later index can be changed using this method |
|           loc[]           |                                                                                            Method retrieves rows based on index label                                                                                            |
|          iloc[]           |                                                                                          Method retrieves rows based on index position                                                                                           |
|           ix[]            |                                     Method retrieves DataFrame rows based on either index label or index position. This method combines the best features of the .loc[] and .iloc[] methods                                      |
|         rename()          |                                                                     Method is called on a DataFrame to change the names of the index labels or column names                                                                      |
|         columns()         |                                                                                  Method is an alternative attribute to change the coloumn name                                                                                   |
|          drop()           |                                                                                    Method is used to delete rows or columns from a DataFrame                                                                                     |
|           pop()           |                                                                                    Method is used to delete rows or columns from a DataFrame                                                                                     |
|         sample()          |                                                                               Method pulls out a random sample of rows or columns from a DataFrame                                                                               |
|        nsmallest()        |                                                                                  Method pulls out the rows with the smallest values in a column                                                                                  |
|        nlargest()         |                                                                                  Method pulls out the rows with the largest values in a column                                                                                   |
|          shape()          |                                                                             Method returns a tuple representing the dimensionality of the DataFrame                                                                              |
|          ndim()           |                                                Method returns an ‘int’ representing the number of axes / array dimensions. Returns 1 if Series, otherwise returns 2 if DataFrame                                                 |
|         dropna()          |                                                                    Method allows the user to analyze and drop Rows/Columns with Null values in different ways                                                                    |
|         fillna()          |                                                                         Method manages and let the user replace NaN values with some value of their own                                                                          |
|          rank()           |                                                                                    Values in a Series can be ranked in order with this method                                                                                    |
|          query()          |                                                                       Method is an alternate string-based syntax for extracting a subset from a DataFrame                                                                        |
|          copy()           |                                                                                      Method creates an independent copy of a pandas object                                                                                       |
|       duplicated()        |                                                                      Method creates a Boolean Series and uses it to extract rows that have duplicate values                                                                      |
|     drop_duplicates()     |                                                                Method is an alternative option to identifying duplicate rows and removing them through filtering                                                                 |
|        set_index()        |                                                                         Method sets the DataFrame index (row labels) using one or more existing columns                                                                          |
|       reset_index()       |                                                        Method resets index of a Data Frame. This method sets a list of integer ranging from 0 to length of data as index                                                         |
|          where()          |                          Method is used to check a Data Frame for one or more condition and return the result accordingly. By default, the rows not satisfying the condition are filled with NaN value                           |

## Series

> class pandas.Series(data=None, index=None, dtype=None, name=None, copy=False, fastpath=False)
> One-dimensional ndarray with axis labels (including time series).

> Labels need not be unique but must be a hashable type. The object supports both integer- and label-based indexing and provides a host of methods for performing operations involving the index. Statistical methods from ndarray have been overridden to automatically exclude missing data (currently represented as NaN).

> Operations between Series (+, -, /, , \*) align values based on their associated index values– they need not be the same length. The result index will be the sorted union of the two indexes.

### Binary operation methods on series:

| FUNCTION |                                                    DESCRIPTION                                                     |
| :------: | :----------------------------------------------------------------------------------------------------------------: |
|  add()   |              Method is used to add series or list like objects with same length to the caller series               |
|  sub()   |           Method is used to subtract series or list like objects with same length from the caller series           |
|  mul()   |           Method is used to multiply series or list like objects with same length with the caller series           |
|  div()   |             Method is used to divide series or list like objects with same length by the caller series             |
|  sum()   |                                Returns the sum of the values for the requested axis                                |
|  prod()  |                              Returns the product of the values for the requested axis                              |
|  mean()  |                               Returns the mean of the values for the requested axis                                |
|  pow()   | Method is used to put each element of passed series as exponential power of caller series and returned the results |
|  abs()   |                Method is used to get the absolute numeric value of each element in Series/DataFrame                |
|  cov()   |                                  Method is used to find covariance of two series                                   |

### Pandas series method:

|    FUNCTION     |                                                                                               DESCRIPTION                                                                                               |
| :-------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|    Series()     |                                        A pandas Series can be created with the Series() constructor method. This constructor method accepts a variety of inputs                                         |
| combine_first() |                                                                              Method is used to combine two series into one                                                                              |
|     count()     |                                                                        Returns number of non-NA/null observations in the Series                                                                         |
|     size()      |                                                                          Returns the number of elements in the underlying data                                                                          |
|     name()      |                                                                   Method allows to give a name to a Series object, i.e. to the column                                                                   |
|   is_unique()   |                                                                        Method returns boolean if values in the object are unique                                                                        |
|    idxmax()     |                                                                 Method to extract the index positions of the highest values in a Series                                                                 |
|    idxmin()     |                                                                 Method to extract the index positions of the lowest values in a Series                                                                  |
|  sort_values()  |                                                            Method is called on a Series to sort the values in ascending or descending order                                                             |
|  sort_index()   |                                                            Method is called on a pandas Series to sort it by the index instead of its values                                                            |
|     head()      |                                        Method is used to return a specified number of rows from the beginning of a Series. The method returns a brand new Series                                        |
|     tail()      |                                           Method is used to return a specified number of rows from the end of a Series. The method returns a brand new Series                                           |
|      le()       |                     Used to compare every element of Caller series with passed series.It returns True for every element which is Less than or Equal to the element in passed series                     |
|      ne()       |                         Used to compare every element of Caller series with passed series. It returns True for every element which is Not Equal to the element in passed series                         |
|      ge()       |                   Used to compare every element of Caller series with passed series. It returns True for every element which is Greater than or Equal to the element in passed series                   |
|      eq()       |                           Used to compare every element of Caller series with passed series. It returns True for every element which is Equal to the element in passed series                           |
|      gt()       |                                                            Used to compare two series and return Boolean value for every respective element                                                             |
|      lt()       |                                                            Used to compare two series and return Boolean value for every respective element                                                             |
|     clip()      |                                                                    Used to clip value below and above to passed Least and Max value                                                                     |
|  clip_lower()   |                                                                             Used to clip values below a passed least value                                                                              |
|  clip_upper()   |                                                                            Used to clip values above a passed maximum value                                                                             |
|    astype()     |                                                                             Method is used to change data type of a series                                                                              |
|    tolist()     |                                                                               Method is used to convert a series to list                                                                                |
|      get()      |                                       Method is called on a Series to extract values from a Series. This is alternative syntax to the traditional bracket syntax                                        |
|    unique()     |                                                                 Pandas unique() is used to see the unique values in a particular column                                                                 |
|    nunique()    |                                                                        Pandas nunique() is used to get a count of unique values                                                                         |
| value_counts()  |                                                              Method to count the number of the times each unique value occurs in a Series                                                               |
|   factorize()   |                                                        Method helps to get the numeric representation of an array by identifying distinct values                                                        |
|      map()      |                                                                      Method to tie together the values from one object to another                                                                       |
|    between()    |                                                  Pandas between() method is used on series to check which values lie between first and second argument                                                  |
|     apply()     | Method is called and feeded a Python function as an argument to use the function on every Series value. This method is helpful for executing custom operations that are not included in pandas or numpy |
