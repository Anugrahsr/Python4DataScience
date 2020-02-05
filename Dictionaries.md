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

