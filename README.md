# DataCleaning-Using-python

## Missing / Null values in a dataset

1. When we say a value is missing or is null, we do not mean that the value is an empty string, such as ' ', or a zero value, such as 0 or 0.0. Missing or null means there is no value present at all.
    
2. For the survey data we are looking at now, it means the person taking the survey provided no answer. When we are representing our data with a series or a dataframe, we can't simply skip missing values, they must be encoded in some way.
   
3. A series with a missing value at the fifth index can't just be one value shorter. It throws off everything. Instead, we need to plug in a special value that represents a missing value so that when we perform operations on the series, nothing goes awry.
   
4. For example, if we ask for the mean value of a series of values that contains some missing values, we would not want to sum all the values and then divide them by the length of the series. The length would include the missing values and throw off the mean value.

## Handling missing values using python 
    
NaN means Not a Number in pandas library. It is a special floating-point value that is different from NoneType in Python. NaN values can be annoying to work with, especially when you want to filter them out for plots or analysis. To make our lives easier, let’s replace these NaN values with some required value.

**Python holds various methods to handle missing values** :
**Pandas library functions**

## 1. fillna( )

   This method is used to fill the required data in the missing value cells. there are various paramaters that comes under this method.

   1.1 fillna( ) with **value** parameter,

   Syntax :-

   **fillna(value = requiredvalue)**
   
   1.2 fillna( ) with **method = pad** parameter,

   This helps to fill the missing values using previous **row** value

   Syntax:-

   **fillna(method = 'pad')**

   In case of previous **column** value requirement,

   Syntax:-

   **fillna(method='pan',axis = 1)**


   1.3 fillna( ) with **method = bfill**

   This is also known as backward fill where the succeding row value is filled in the area of missing values

   Syntax:-

   **fillna(method = 'bfill')**

   In case of suceeding **column** value requirement,

   Syntax:-

   **fillna(method='bfill',axis = 1)**
   

   1.4 fillna( ) with filling desired values seperately for required columns

   This is achieved by using the **dictionary** data type which holds key and value pairs. The key is considered to be the name of the column present in the dataset and value will be 
   considered as the desired value that must be filled in particular keys alone.

   Syntax:-

   **fillna({key1 :value1 , Key2 : value2})**

   1.5 fillna( ) with **central tendency measures** - Mean . Median and Mode

   Syntax:-

   **fillna(value = df['columnname'].mean())**
   **fillna(value = df['columnname'].median())**
   **fillna(value = df['columnname'].mode())**
   **fillna(value = df['columnname'].min())**
   **fillna(value = df['columnname'].max())**

## 2. Dropping Null values
   

   




   


