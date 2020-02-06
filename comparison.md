# Comparison operator
---
**comparison types**

| operator | Use |
|----------|-----|
| <        |less than|
| >| greater than|
|<=|less than or equal|
|>=|greater than or equal|
|==|equal|
|!= |mot equal|

<br>

**Bool Operators**

|Operator|Operation|
|---|--|
|AND|Returns True if both statements are true|
|OR|Returns True if one of the statements is true|
|NOT|Reverse the result, returns False if the result is true|

Example:

```python
True and True
#output: True
#others are false
```

We can not use and, or and not in array
we use array equvalent of bool operator such as
```logical_and```, ```logical_or``` and ```logical_not```


```python
# Define variables
my_kitchen = 18.0
your_kitchen = 14.0

# my_kitchen bigger than 10 and smaller than 18?
print(my_kitchen > 10 and my_kitchen < 18)

# my_kitchen smaller than 14 or bigger than 17?
print(my_kitchen < 14 or my_kitchen > 17 )

# Double my_kitchen smaller than triple your_kitchen?
print(2 * my_kitchen < 3 * your_kitchen)
```

**Numpy**

```python
import numpy as np
```

example

```python
# Create arrays
import numpy as np
my_house = np.array([18.0, 20.0, 10.75, 9.50])
your_house = np.array([14.0, 24.0, 14.25, 9.0])

# my_house greater than 18.5 or smaller than 10
print(np.logical_or(my_house > 18.5,my_house <10))

# Both my_house and your_house smaller than 11
print(np.logical_and(my_house < 11, your_house < 11))
```
**if elif else**

![image](https://hcc-cs.weebly.com/uploads/2/4/5/3/24535251/1390049468.jpg)

---

example

```python
# Define variables
room = "kit"
area = 14.0

# if-else construct for room
if room == "kit" :
    print("looking around in the kitchen.")
else :
    print("looking around elsewhere.")

# if-else construct for area
if area > 15 :
    print("big place!")
else :
    print("pretty small")
```
**Elif**

```python
# Define variables
room = "bed"
area = 14.0

# if-elif-else construct for room
if room == "kit" :
    print("looking around in the kitchen.")
elif room == "bed":
    print("looking around in the bedroom.")
else :
    print("looking around elsewhere.")

# if-elif-else construct for area
if area > 15 :
    print("big place!")
elif area > 10 :
    print('medium size, nice!')
else :
    print("pretty small.")
```

**Filtering Pandas DataFrame**

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Extract drives_right column as Series: dr
dr = cars["drives_right"]

# Use dr to subset cars: sel
sel = cars[dr]

# Print sel
print(sel)
```

Example:

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Import numpy, you'll need this
import numpy as np

# Create medium: observations with cars_per_cap between 100 and 500
cpc = cars['cars_per_cap']
between = np.logical_and(cpc >100, cpc <500)
medium = cars[between]


# Print medium
print(medium)
```
**while loop**

```
while condition :
    expression
```

example

```python
x = 1
while x < 4 :
    print(x)
    x = x + 1
```

example
if else in a while loop

```python
# Initialize offset
offset = -6

# Code the while loop
while offset != 0 :
    print("correcting...")
    if offset > 0 :
        offset = offset -1
    else : 
        offset = offset +1
    print(offset)
  ```
  
**For Loops**

```python
for var in seq:
    expression
```

example

```python
fam = [1.73, 1.68, 1.71, 1.89]
for height in fam : 
    print(height)
```

Using a ```for``` loop to iterate over a list only gives you access to every list element in each run, one after the other. If you also want to access the index information, so where the list element you're iterating over is located, you can use ```enumerate()```
 
 example
 
 ```python
 fam = [1.73, 1.68, 1.71, 1.89]
for index, height in enumerate(fam) :
    print("person " + str(index) + ": " + str(height))
```

example
we can use ```x[0]``` and ```x[1]``` to navigate the array

```python
# house list of lists
house = [["hallway", 11.25], 
         ["kitchen", 18.0], 
         ["living room", 20.0], 
         ["bedroom", 10.75], 
         ["bathroom", 9.50]]
         
# Build a for loop from scratch
for x in house:
    print("the " + x[0] + " is " + str(x[1]) + " sqm")
```
# Loop over dictionary

In Python 3, you need the ```items()``` method to loop over a dictionary:
```python
world = { "afghanistan":30.55, 
          "albania":2.77,
          "algeria":39.21 }

for key, value in world.items() :
    print(key + " -- " + str(value))
```

# Loop over Numpy array

```python
#1D array
for x in my_array :
    ...
```

```python
#2D array
for x in np.nditer(my_array) :
    ...
```

for multi-dimensional array we need to use ```np.nditer```

example:

```python
# Import numpy as np
import numpy as np

# For loop over np_height
for x in np.nditer(np_height):
    print(str(x) + " inches")

# For loop over np_baseball
for k in np.nditer(np_baseball):
    print(k)
```

# Loop over DataFrame

Iterating over a Pandas DataFrame is typically done with the ```iterrows()``` method

```python
for lab, row in brics.iterrows() :
    print(row['country'])
```

example

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Adapt for loop
for lab, row in cars.iterrows() :
    print(lab + ": " + str(row["cars_per_cap"]))
```
new column

```python
for lab, row in brics.iterrows() :
    brics.loc[lab, "name_length"] = len(row["country"])
```
Apply method as replacement

```python
for lab, row in brics.iterrows() :
    brics.loc[lab, "name_length"] = len(row["country"])
```

```python
brics["name_length"] = brics["country"].apply(len)
```
