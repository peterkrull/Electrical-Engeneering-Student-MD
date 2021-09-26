status :: #red 

# Lists in Python

\#python #list #array

---

## Creating a list

````Python
>>> a = [] # creates an empty list
>>> b = [1,2,3,4] # creates a list
````

---

## Appending to a list

````Python
>>> a.append("Hello")
>>> a.append("world")
>>> print(a)
["Hello","world"]
````

---

## Indexing a list

Most [programming](../Programming.md) languages [index](../0%20and%201%20indexing.md) from 0. What this means is that the first entry in the list, exists at the 0th place in the list, the second in the 1st, third in the 2nd and so forth. This will often confuse both beginner and experienced programmers

````Python
#          0th	   1st     2nd     3rd
>>> b = ["Johan","Peter","Sarah","Aleks"]
>>> b[2] # returns the "third" entry existing in the 2nd place
'Sarah'
````

When you have multi-dimensional or "nested" lists, indexing happens in an outside-in fashion. This means that in the example below `b[x][y]`, the entry `x` returns either of the two lists within `b`, namely the name or the occupation list, and `y` returns the corresponding index within the `x` list.

````Python
>>> b = [
		["Johan","Peter","Sarah","Aleks"],
		["Janitor","Student","Chemist","Mechanic"]
		]

# returns entries in place x,y
>>> print (f"{b[0][2]} is a {b[1][2]}")
'Sarah is a Chemist'

# returns entire x-level list
>>> print ( b[0] )
["Johan","Peter","Sarah","Aleks"]
````

---

## Iterate through lists

*Python syntax* is fairly unique that allows us to write some pretty handy code. Take this example, where we are able to iterate through the list using a *for-loop* where the iterator of the for loop is not just the index of the list, but the actual entry of the list.

````Python
# Better method
>>> b = ["Johan","Peter","Sarah","Aleks"]
>>> for name in b:
>>>		if name == "Peter":
...			print (name + ", please stand up")
...
'Peter, please stand up'
````

Compare this to the following example. The difference is small, but having to index the list correctly just adds another layer of complexity that is not needed, and the code just looks more messy. The functionality of the code is the exact same in this case.

````Python
# "Traditional" method
>>> b = ["Johan","Peter","Sarah","Aleks"]
>>> for index in range(len(b)):
>>>		if b[index] == "Peter":
...			print (b[index] + ", please stand up")
...
'Peter, please stand up'
````
