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
