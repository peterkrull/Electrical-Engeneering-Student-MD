status :: #yellow

# Markdown syntax

\#markdown #obsidian #syntax

## Images

|![](obsidian.png)|![obsidian.png](../../XX_Images/obsidian.png)|
|::|:----------:|
|Regular markdown images|Obsidian specific images|

---

## Code snippets

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

---

## Tables

|Tables|Are|Cool|
|------|:-:|---:|
|col 3 is|right-aligned|$1600|
|col 2 is|centered|$12|
|zebra stripes|are neat|$1|

---

## Quotes

 > 
 > Happy birthday, Harry

---

## HTML

<dl>
 <dt>Definition list</dt>
 <dd>Is something people use sometimes.</dd>
<dt>Markdown in HTML</dt>
 <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

---

# Obsidian specific syntax

[Obsidian](../Obsidian.md) adopts all of the regular markdown syntax, but adds a few more important ones.

### Linking

Linking to other notes in Obsidian is done by using double square brackets \[\[\]\] around some string of characters. It will look like this : [markdown syntax](markdown%20syntax.md)
