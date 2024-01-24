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

**Multi variable** `x,y,z = 'Amit','Inderjeet','Vipul'`

**One value to multiple** `x=y=z='Amit`

**To unpack a list**
fruits = ['apple', 'orange', 'pears']
x,y,z =fruits

**In print you can use comma and plus to output multiple variables**

`print(x,y)`

`print(x+y)`

*Global Variable can be defined using `global x`*

## Data Types

`Text - str`

`Numeric -  int, float, complex`

`Sequence Type - list, tuple, range`

`Mapping - dict`

`None Type - Nonetype`

`set type - set, fronzenset`

*Note: You can convert int to float and float to int.*


Random number - python got no random number function.
`
import random
print(random.randrange(1,10))
print(random.randrange(1,10000000))
`

**Note: Strings are array**

**Looping through string**
`
for x in 'Amit':
  print(x)
`
***get length of string***
`
print(len(a))
`

Check substring in string

`
txt = "The quick brown fox jumps over the lazy dog"
if 'a' in txt:
  print('true')
`

***Slicing string***
The first character has index 0.
a = "Hello World"

print(a[2:5]) # llo


**Negative Indexing**

`print(a[-5:-2]) # Wor`

**Modify string**

```
a = ' Hello World'
print(a.upper())
print(a.lower())
print(a.strip()) # remove whitespace from beginning and end
print(a.replace("H","j"))  # replace is case sensitive
print(a.split(",")
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

``** Exponentiation``
``// Floor Division``

```
1. Almost any value is evaluated to True if it has some sort of content.
2. Any string is True, except empty strings.
3. Any number is True, except 0.
4. Any list, tuple, set, and dictionary are True, except empty ones.
5. In fact, there are not many values that evaluate to False, except empty values, such as (), [], {}, "", the number 0, and the value None. And of course the value False evaluates to False.
```

Identity Operator are used used to compare objects, not if they are equal, but if they are actually the same object, with the same memory location:
`is : x is y`
`is not : x is not y`

Membership Operator are used to test if a sequence is present in an objects:
`in `
`not in`
```
 x =['apple','banana']
 print('banana in x)
```

Bitwise opearator
```
AND(&) - Sets each bit to 1 if both bits are 1
OR (|) 	- Sets each bit to 1 if one of two bits is 1
XOR(^) -	Sets each bit to 1 if only one of two bits is 1	x ^ y	
NOT(~) -	Inverts all the bits
```

Precedence order
![image](https://github.com/amit140507/python-basics/assets/100019842/95147ec3-ebbc-4b01-a729-1902e1f9f2f1)


| Data Type  | Mutable | Ordered | Indexed | Allow Duplicate|
| ------------- | ------------- | ------------- | ------------- |------------- |
| List  | Y  | Y  | Y  | Y  |
| Tuple  | N  | Y  | - | Y  |
| Set  |  Y  | N  | N  | N  |
| Frozenset  |  N  | N  | N  | N  |
| Dictionary |  Y  | Y  | - | N  |

> :spiral_notepad: Set items are unchangeable, but you can remove and/or add items whenever you like.
## Python Lists
```
mylist = ['apple','grapes','oranges', 'pears', 'guava']
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

**-get data type**
```
print(type(mylist))
```
**- create new list**
```
newlist = list(("apple","banana", "grapes"))
print(newlist)
```

**list** `x = ["apple", "banana", "cherry"]`

**tuple** `x = ("apple", "banana", "cherry")`

**range** `x = range(6)`

**set** = `x = {"apple", "banana", "cherry"}`

**dict** `x = {"name" : "John", "age" : 36}`

**frozenset** `x = frozenset({"apple", "banana", "cherry"})`

## Access Items
- with index
- negative index means start from the end (-1 is last item)

**range of index**
`
print(newlist[2:5]
`
> Range start from 2(included) and end on 5(not incuded)

**check if item exists**
`
if ("apple" in thislist)
  print("Yes")
`
**-Change Item value**
`
newlist = ["apple","banana","grapes"]
newlist[0] = "kiwi"
print(newlist)
`

**change range of item values**
`
newlist[1:3] = ["kiwi","cocunut"]
`



























