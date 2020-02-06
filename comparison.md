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
  
  
    
