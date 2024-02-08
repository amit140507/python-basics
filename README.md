# python-basics

### How to declare a variable?
Can create by just assigning the value or by casting

`x = str(3)`

*Note:* 
1. variables are case sensitive
2. start with letter or underscore
3. cannot start with number
4. can only contain alpha numeric and underscore
5. cannot be python keywords

**Multi variable**   
```
x,y,z = 'Amit','Inderjeet','Vipul'
```

**One value to multiple**  
```x=y=z='Amit```

**To unpack a list**
```
fruits = ['apple', 'orange', 'pears']
x,y,z =fruits
```

**In print you can use comma and plus to output multiple variables**

`print(x,y)`

`print(x+y)`

*Global Variable can be defined using `global x`*

## Data Types

**Text** - `str`

**Numeric** -  `int, float, complex`

**Sequence Type** - `list, tuple, range`

**Mapping** - `dict`

**None Type** - `Nonetype`

**set type** - `set, fronzenset`

*Note: You can convert int to float and float to int.*

**Random number** - python got no random number function.
```
import random
print(random.randrange(1,10))
print(random.randrange(1,10000000))
```

>Note: **Strings are array**

**Looping through string**
```
for x in 'Amit':
  print(x)
```

**get length of string**
```
txt = "The quick brown fox jumps over the lazy dog"
print(len(txt))
```

**Check substring in string**
```
txt = "The quick brown fox jumps over the lazy dog"
if 'a' in txt:
  print('true')
```

**Slicing string**
```
a = "Hello World"
print(a[2:5]) # llo
```
> Note: The first character has index 0.

**Negative Indexing**
```
print(a[-5:-2]) # Wor
```

**Modify string**

```
a = ' Hello:World'
print(a.upper())
print(a.lower())
print(a.strip()) # remove whitespace from beginning and end
print(a.replace("H","j"))  # replace is case sensitive
print(a.split(":"))
```
**We can combine string and number by using `format()`**
```
age =35
name = 'Amit'
txt = "My age is {} and name is {}"
print(txt.format(age, name))
```

**Using Index**
```
txt = " I am {0} year old and born in {1}"
year = 1999
age = 23
print(txt.format(age, year))
```

**Escape character**

`\n  - newline`

`\r  - carriage return`

`\t  - tab`

`\b  - backspace`


All string method return new values.They do not change original string.

## Python Operator


**`**`** - Exponentiation

**`//`** - Floor Division

+ Almost any value is evaluated to True if it has some sort of content.
+ Any string is True, except empty strings.
+ Any number is True, except 0.
+ Any list, tuple, set, and dictionary are True, except empty ones.
+ In fact, there are not many values that evaluate to False, except empty values, such as (), [], {}, "", the number 0, and the value None. And of course the value False evaluates to False.


**Identity Operator** are used used to compare objects, not if they are equal, but if they are actually the same object, with the same memory location:

**is**
```
x is y
```
**is not**
```
x is not y
```

**Membership Operator** are used to test if a sequence is present in an objects:

**in**
**not in**
```python
x =['apple','banana']
print('banana in x)
```

**Bitwise opearator**


AND(&) - Sets each bit to 1 if both bits are 1

OR (|) 	- Sets each bit to 1 if one of two bits is 1

XOR(^) -	Sets each bit to 1 if only one of two bits is 1	x ^ y	

NOT(~) -	Inverts all the bits


Precedence order
![image](https://github.com/amit140507/python-basics/assets/100019842/95147ec3-ebbc-4b01-a729-1902e1f9f2f1)


| Data Type  | Mutable | Ordered | Indexed | Allow Duplicate|
| ------------- | ------------- | ------------- | ------------- |------------- |
| List  | Y  | Y  | Y  | Y  |
| Tuple  | N  | Y  | Y | Y  |
| Set  |  Y  | N  | N  | N  |
| Frozenset  |  N  | N  | N  | N  |
| Dictionary |  Y  | Y  | - | N  |

> :spiral_notepad: Set items are unchangeable, but you can remove and/or add items whenever you like.

**list** `x = ["apple", "banana", "cherry"]`

**tuple** `x = ("apple", "banana", "cherry")`

**range** `x = range(6)`

**set** = `x = {"apple", "banana", "cherry"}`

**dict** `x = {"name" : "John", "age" : 36}`

**frozenset** `x = frozenset({"apple", "banana", "cherry"})`

## Python Lists
```
x = ["apple", "banana", "cherry"]
x = list(("apple", "banana", "cherry"))
print(mylist)
```

- New item add in the end of list.
- list has defined order, and that order will not change.
- we can add or remove items from list after its creation.
- it is indexed, list can have duplicate values.

**Get length of list**
```
print(len(mylist))
```

**list can have different data types**
```
mylist = ['Amit', 1, True]
```

**get data type**
```
print(type(mylist))
```
**create new list**
```
newlist = list(("apple","banana", "grapes"))
print(newlist)
```
### Access Items
- with index
- negative index means start from the end (-1 is last item)

**range of index**
```
print(newlist[2:5]
```
> Range start from 2(included) and end on 5(not incuded)

**check if item exists**
```
if ("apple" in thislist)
  print("Yes")
```
**Change Item value**
```
newlist = ["apple","banana","grapes"]
newlist[0] = "kiwi"
print(newlist)
```
**change range of item values**
```
newlist[1:3] = ["kiwi","cocunut"]
```

> if you insert more items that you replace, the new items will be inserted  where you specified and remaining will move accordingly.
> If you insert less item than you replace, the new items will insert where you specified and remaining will move accordingly.

**Insert new item without replacing existing items**
```
thislist.insert(2,"watermelon")
print(thislist)
```
**Append an item**
```
thislist.append("orange")
```
**To extend elements of another list to the current list, use extend()**
```
thislist= ['x','y','z']
newlist = ['a','b','c']
thislist.extend(newlist)
print(thislist)
```

> **You can use it to extend any  iterable objects(tuple, set, dictionaries)**

**remove an item**
```
newlist = ['a','b','c']
newlist.remove("a")
print(newlist)
```
**POP** - to remove a specific index
```
thislist = ['a','b','c','d']
thislist.pop(1)
print(thislist)
thislist.pop()
print(thislist)
```
> **If you don't specify, pop method remove the last item**

**del** - keyword also remove the specific index
```
del.thislist[0]
print(thislist)
```
**delete the entire list**
```
del thislist
print(thislist)
```
**clear** - to empty the list
>This list remains but it has no content.
```
thislist.clear[]
print(thislist)
```

### Loop a list
```
thislist = ['A','B','C','D']
for x in thislist:
  print(x)
```
**Looping through  index numbers**
**range() and len()**
```
thislist = ["apple", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i])
```
**Using a While Loop**
```python
thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1
```
**Looping using list Comprehension**
```
[print(x) fo x in thilist]
```
**List Comprehesion** offer shortest syntax when you want to create a new list based on the values
```
fruits = ['apple','banana','grapes','kiwi']
newlist = []
for x in fruits:
  if "a" in x:
    newlist.append(x)
print(newlist)
```

```
newlist = [x for x in fruits if "a" in x]
print(newlist)
```
**syntax**
>  newlist = [expression for item in iterable if condition]
> return value is new list, old one remain unchanged.


**Filter(if)**
```
newlist = [x for x in fruits if x != 'apple']
print(newlist)
```

**Iterable**
```
newlist = [x for x in range(10)]
print(newlist)

newlist = [x for x in range(10) if x < 5]
print(newlist)
```

**Expression** is the current item in the iteration, but it is also the outcome which you can manipulate before it ends up like a list item in the newlist.
```
newlist = [x.upper() for x in fruits]
print(newlist)

newlist = ['hello' for x in fruits]
print(newlist)
```
```
newlist = [x if x != 'apple' else orange for x in fruits]
print(newlist)

```
**Sort list** 
Aplhabetically
```
 thislist.sort() -  ascending
 thislist.sort(reverse = true) - decending
```
**Case sensitive sort** By default the sort() method is case sensitive, resulting in all capital letters being sorted before lower case letters:
```
thislist.sort() # case sensitive
thislist.sort(key= str.lower) # case insensitive
print(thislist)
```
**Reverse Order** -  reverse current sorting order
```
thislist.reverse()
print(thislist)
```

### Copy Lists
> You can't copy by using list1= list2

**Method 1: copy()**
```
mylist = thislist.copy()
```
**Method 2: list()**
```
mylist = list(thilist)
```

### Join two lists

using **+** operator
```
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)
```

using **append**
```
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]
for x in list2:
  list1.append(x)
print(list1)
```
or 
```
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list1.extend(list2)
print(list1)
```
**List Methods**

| Method  | Description |
| ------------- | ------------- |
| append()  | Adds an element at the end of the list |
| clear()  | Removes all the elements from the list  |
| copy() |	Returns a copy of the list |
| count()	| Returns the number of elements with the specified value |
| extend()	| Add the elements of a list (or any iterable), to the end of the current list |
| index()	| Returns the index of the first element with the specified value |
| insert()	| Adds an element at the specified position |
| pop()	| Removes the element at the specified position |
| remove()	| Removes the item with the specified value |
| reverse()	| Reverses the order of the list |
| sort()	| Sorts the list |


## tuples
```
x = ("apple", "banana", "cherry")
x = tuple(("apple", "banana", "cherry"))
```

-tuple are ordered, unchangeable and allow duplicate values. Tuple are indexed.
-Order cannot get changed in tuple.
- tuple are unchangeable
- tuples are indexed.

**len()** is used to determine the length of tuple
```
thistuple = ("apple", "banana", "cherry")
print(len(thistuple))
```
**Create tuple with one item**
To create a tuple with only one item, you have to add a comma after the item, otherwise Python will not recognize it as a tuple.
```
thistuple = ("apple",)
print(type(thistuple))
```

- tuple can have any data types

**The tuple() Constructor**
```
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(thistuple)
```
**Access tuple items**
- using index
```
thistuple[1]
```
-Negative Indexing
```
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])
```
-Range of Indexes
```
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])
```

>**Note:** The search will start at index 2 (included) and end at index 5 (not included).

-Range of Negative Indexes
```
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[-4:-1])
```
**-Check if Item Exists**
```
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple")
```

### Update Tuples

- tuples are unchangeable and immutable
```python
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)
```

### Add Items
> Since tuples are immutable, they do not have a built-in append() method.
1. Convert into a list: Just like the workaround for changing a tuple, you can convert it into a list, add your item(s), and convert it back into a tuple.
```
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)
```
2. Add tuple to a tuple. You are allowed to add tuples to tuples, so if you want to add one item, (or many), create a new tuple with the item(s), and add it to the existing tuple:
```
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y

print(thistuple)
```

**Remove Items**
```python
thistuple = ("apple", "banana", "cherry")
y =list(thistuple)
y.remove = ("apple")
thistuple = tuple(y)
print(thistuple)
```
**Delete** the tuple completely
```
thistuple = ("apple", "banana", "cherry")
del thistuple
print(thistuple)
```

### Unpack tuples
when we create a tuple we normally assign values to it.This is called packing of tuple.

**Packing a tuple**
```
fruits = ("apple", "banana", "cherry")
```
**Unpacking a tuple**
```
fruits = ("apple", "banana", "cherry")
x,y,z = fruits
print(x, y, z)
```
>The number of variable must match the number of values in the tuple, if not, you must use an asterisk to collect the remaining values as a list.
Assign the rest of the values as a list called red:
```
fruits = ("apple", "banana", "cherry")
x,*y =  fruits
print(x)
print(y)
```
> If the asterisk is added to another variable name than te last one, python will assign values to the variable until the number of values left matches the number of vaariable left.

**Loop tuples**
```python
thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)
```

**Loop through index numbers** using range() of len() function
```
thistuple = ("apple", "banana", "cherry")
for i in range(len(thistuple)):
  print(thistuple[i])
```
**While loop**
```
thistuple = ("apple","banana","grapes")
i=0
while i<len(thistuple):
  print(thistuple[i]
i += 1
```

**Join Tuples**
```
tuple1 = ("a","b","c")
tuple2 = ("e","f","g")
tuple3 = tuple1 + tuple2
print(tuple3)
```

**Multiply values use * operator**
```
fruits =  ("apple","banana","grapes")
newfruits = fruits*2
print(newfruits)
```

**Tuple methods**


| Method |	Description|
| ------------- | ------------- |
| count() |	Returns the number of times a specified value occurs in a tuple |
| index() |	Searches the tuple for a specified value and returns the position of where it was found |

**count()**
```
thistuple = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
x = thistuple.count(5)
print(x)
```
**index()**
```
thistuple = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
x = thistuple.index(8)
print(x)
```

## Python sets
```
x = {"apple", "banana", "cherry"}
x = set(("apple", "banana", "cherry"))
```
> Note: Set items are unchangeable, but you can remove items and add new items.
> Note: Sets are unordered, so you cannot be sure in which order the items will appear.
> Set items are unordered, unchangeable, and do not allow duplicate values.
> Set items can appear in a different order every time you use them, and cannot be referred to by index or key.
> Sets cannot have two items with the same value.
> Note: The values True and 1 are considered the same value in sets, and are treated as duplicates.
> Once a set is created, you cannot change its items, but you can remove items and add new items.
> Set can have any data types
> 
**Get the Length of a Set**
```
thisset = {"apple", "banana", "cherry"}
print(len(thisset))
```
**Access Items**cannot access items in a set by referring to an index or a key. But you can loop through the set items.
thisset ={'apple', 'banana','cherry'}
```
for x in thisset:
  print(x)
```
```
thisset = {"apple", "banana", "cherry"}
print("banana" in thisset)
```
**Change Items**
>Once a set is created, you cannot change its items, but you can add new items.

**Add Items**
```
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset)
```
**Add sets**
```
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}
thisset.update(tropical)
print(thisset)
```

**Add Any Iterable**
The object in the update() method does not have to be a set, it can be any iterable object (tuples, lists, dictionaries etc.).
```
thisset = {"apple", "banana", "cherry"}
mylist = ["kiwi", "orange"]
thisset.update(mylist)
print(thisset)
```

**Remove Item**
```
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)
```

>Note: If the item to remove does not exist, remove() will raise an error.

```
thisset = {"apple", "banana", "cherry"}
thisset.discard("banana")
print(thisset)
```
>Note: If the item to remove does not exist, discard() will NOT raise an error.


>You can also use the pop() method to remove an item, but this method will remove a random item, so you cannot be sure what item that gets removed.
The return value of the pop() method is the removed item.

```
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x)
print(thisset)
```

The clear() method empties the set:
```
thisset = {"apple", "banana", "cherry"}
thisset.clear()
print(thisset)
```

The del keyword will delete the set completely:
```
thisset = {"apple", "banana", "cherry"}
del thisset
print(thisset)
```

### Loop Sets

```
thisset = {"apple", "banana", "cherry"}
for x in thisset:
  print(x)
```
### Join Two Sets
>The union() method returns a new set with all items from both sets:
```
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)
```

>The update() method inserts the items in set2 into set1:
```
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set1.update(set2)
print(set1)
```
**Keep ONLY the Duplicates**
>The intersection_update() method will keep only the items that are present in both sets.
```
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
x.intersection_update(y)
print(x)
```
>The intersection() method will return a new set, that only contains the items that are present in both sets.
```
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.intersection(y)
print(z)
```

**Keep All, But NOT the Duplicates**
>The symmetric_difference_update() method will keep only the elements that are NOT present in both sets.
```
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
x.symmetric_difference_update(y)
print(x)
```

>The symmetric_difference() method will return a new set, that contains only the elements that are NOT present in both sets.
```
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.symmetric_difference(y)
print(z)
```




**Set Methods**
|Method|	Description|
| ------------- | ------------- |
|add() |	Adds an element to the set|
|clear() |	Removes all the elements from the set|
|copy()	| Returns a copy of the set|
|difference()	| Returns a set containing the difference between two or more sets|
|difference_update()	| Removes the items in this set that are also included in another, specified set|
|discard()	 | Remove the specified item|
|intersection()  |	Returns a set, that is the intersection of two other sets|
|intersection_update()  |	Removes the items in this set that are not present in other, specified set(s)|
|isdisjoint()	 |Returns whether two sets have a intersection or not|
|issubset()	 |Returns whether another set contains this set or not|
|issuperset() |	Returns whether this set contains another set or not|
|pop()	 |Removes an element from the set|
|remove() |	Removes the specified element|
|symmetric_difference() |Returns a set with the symmetric differences of two sets|
|symmetric_difference_update()	 |inserts the symmetric differences from this set and another|
|union()	 |Return a set containing the union of sets|
|update()	 |Update the set with the union of this set and others|
































