# DataFrame

The DataFrame is one of Pandas most important data structures.

**What is Pandas ?**
<br>
![[pandas]](https://miro.medium.com/max/1080/1*_oSOImPmBFeKj8vqE4FCkQ.jpeg)

[pandas](https://pandas.pydata.org/)
is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool, built on top of the Python programming language
<br>
---
**Importing Pandas**

```python
import pandas as pd
```
people in the community use the alias pd for pandas when importing the library

---

**Creating DataFrame from Dictionary**

```python
df = pd.DataFrame(my_dict)
```

Example

```python
# Pre-defined lists
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr =  [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]

# Import pandas as pd
import pandas as pd 

# Create dictionary my_dict with three key:value pairs: my_dict

my_dict = {'country' : names,
'drives_right' : dr,
'cars_per_cap' : cpc}
# Build a DataFrame cars from my_dict: cars
cars = pd.DataFrame(my_dict)

# Print cars
print(cars)
```

output:
```
 cars_per_cap        country  drives_right
0           809  United States          True
1           731      Australia         False
2           588          Japan         False
3            18          India         False
4           200         Russia          True
5            70        Morocco          True
6            45          Egypt          True
```

**Changing row index**

Specify the row labels by setting cars.index equal to row_labels
```python
# Definition of row_labels
row_labels = ['US', 'AUS', 'JPN', 'IN', 'RU', 'MOR', 'EG']
cars.index = row_labels
```
output:

```
     cars_per_cap        country  drives_right
US            809  United States          True
AUS           731      Australia         False
JPN           588          Japan         False
IN             18          India         False
RU            200         Russia          True
MOR            70        Morocco          True
EG             45          Egypt          True
```
Now its easy to identify the rows right?

---

 data is typically available as files with a regular structure. One of those file types is the CSV file, which is short for "comma-separated values".
 
 To import CSV data into Python as a Pandas DataFrame you can use ```read_csv()```.
 
 ```python
 import pandas as pd
 df = pd.read_csv('data.csv')
 ```
**row labeling**

we can use ```index_col=0``` to fix this

```python
# Fix import by including index_col
cars = pd.read_csv('cars.csv', index_col=0)
```

---

Use single square brackets to print out ```Pandas Series```
Use double square brackets to print out ```Pandas DataFrame```

Example
```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out country column as Pandas Series
print(cars['country'])

# Print out country column as Pandas DataFrame
print(cars[['country']])

# Print out DataFrame with country and drives_right columns
print(cars[['country','drives_right']])
```
```cars[0:5]``` will give you first 5 observations

examples
```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out first 3 observations
print(cars[0:3])

# Print out fourth, fifth and sixth observation
print(cars[3:6])
```
output:
```
     cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JPN           588          Japan         False
    
    
         cars_per_cap  country  drives_right
    IN             18    India         False
    RU            200   Russia          True
    MOR            70  Morocco          True

```

**loc and iloc**

 loc and iloc you can do practically any data selection operation on DataFrames
 
 ```python
 cars.loc['RU']
cars.iloc[4]

cars.loc[['RU']]
cars.iloc[[4]]

cars.loc[['RU', 'AUS']]
cars.iloc[[4, 1]]
```
```loc``` and ```iloc``` also allow you to select both rows and columns from a DataFrame. 
 
```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
# Print out drives_right value of Morocco
print(cars.loc['MOR','drives_right'])
#print(cars.iloc[-2,-1])
# Print sub-DataFrame
cars.loc[['RU','MOR'],['country','drives_right']]
#cars.iloc[[-2,-3],[-2,-1]]
```

It's also possible to select only columns with loc and iloc. In both cases, you simply put a slice going from beginning to end in front of the comma:

```
cars.loc[:, 'country']
cars.iloc[:, 1]

cars.loc[:, ['country','drives_right']]
cars.iloc[:, [1, 2]]
```
