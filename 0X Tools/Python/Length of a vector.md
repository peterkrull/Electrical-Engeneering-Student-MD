status :: #green 

# Calculating the length of a vector

\#python #programming #vector

In [Python](Python.md), a common way to represent a vector is using a [list](python%20list.md). Do keep in mind however that these vectors with be [0-indexed](../../0%20and%201%20indexing.md), instead of the [1-indexing](../../0%20and%201%20indexing.md) we know from mathematics, and tools such as [Matlab](../Matlab/Matlab.md)

````python
def func(inputs:list):
	if type(inputs) == list:
		sum = 0
		for i in inputs:
			sum += i**2
		import math
		return math.sqrt(sum)
	else:
		return inputs
````

**Example of use**

````python
>>> func([3,4])
5
````
