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
