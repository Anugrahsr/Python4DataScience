# Dictionaries
**What is motivation for learning ?**
``` python
# Definition of countries and capital
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']

# Get index of 'germany': ind_ger
ind_ger = countries.index('germany')

# Use ind_ger to print out capital of Germany
capitals[ind_ger] 
```

As you can see accessing data from array is difficut now, we need to get the index and then the value from the next array.
Oops! too much work right?

**What is a dictionary ?**
<p>
Dictionary in Python is an unordered collection of data values, used to store data values like a map, which unlike other Data Types that hold only single value as an element, Dictionary holds key:value pair. Key value is provided in the dictionary to make it more optimized. </p>
[source](https://www.geeksforgeeks.org/python-dictionary)

![image](https://techeplanet.com/wp-content/uploads/2018/12/python-dictionary.jpg)
---
**Keys**
<br>
If the keys of a dictionary are chosen wisely, accessing the values in a dictionary is easy and intuitive.
using the ``` keys() ``` method, we can find all the keys of the dictionary
``` python
# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Print out the keys in europe
print(europe.keys())
```
output:
```
dict_keys(['france', 'norway', 'spain', 'germany'])
```
<br>

**Value**

<br>
In order to get the value corresponding to a key in python dictionary we can use dictionary name and key
<br>
example

``` python
# Print out value that belongs to key 'norway'
print(europe['norway'])
```
output:

``` 'oslo' ```

! Keys are immutable objects : contants of immutable object can not be changed once created
<br>
## Dictionary manipulation
---
 **Add a new key-value pair**
 
 ``` python
 #Add a key-value pair in dictionary my_dict
 my_dict['key'] = 'value'
 ```
 **Check if a key is present in dictionary**
 ``` python
 print('key' in my_dict)
 #Output will be True or False
 ```
 **Update a existing key-value**
 
 ``` python
 my_dict['key'] = 'value2'
 #the value of key changed from value to value2
 ```
 
 **Remove a key value pair**
 
 ```python
 del(my_dict['key'])
 #removed key from the my_dict
 ```
 ---
 ***Example***
 
 ```python
 # Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'bonn',
          'norway':'oslo', 'italy':'rome', 'poland':'warsaw',
          'australia':'vienna' }

# Update capital of germany
europe['germany'] = 'berlin'

# Remove australia

del(europe['australia'])
# Print europe
print(europe)
```
output:

```python
 {'germany': 'berlin', 'italy': 'rome', 'france': 'paris', 'norway': 'oslo', 'spain': 'madrid', 'poland': 'warsaw'}
```
---
! Dictionaries can contain key:value pairs where the values are again dictionaries.

```python
# Dictionary of dictionaries
europe = { 'spain': { 'capital':'madrid', 'population':46.77 },
           'france': { 'capital':'paris', 'population':66.03 },
           'germany': { 'capital':'berlin', 'population':80.62 },
           'norway': { 'capital':'oslo', 'population':5.084 } }
```

 chained square brackets can be used to navigate the key-value of the Dictionary of dictionaries
 
 ```python
 # Print out the capital of France
print(europe['france']['capital'])
```

output: 
```paris```

**Example**

```python
# Dictionary of dictionaries
europe = { 'spain': { 'capital':'madrid', 'population':46.77 },
           'france': { 'capital':'paris', 'population':66.03 },
           'germany': { 'capital':'berlin', 'population':80.62 },
           'norway': { 'capital':'oslo', 'population':5.084 } }


# Print out the capital of France
print(europe['france']['capital'])

# Create sub-dictionary data
data = {'capital':'rome','population':59.83}

# Add data to europe under key 'italy'
europe['italy'] = data

# Print europe
print(europe)
```
