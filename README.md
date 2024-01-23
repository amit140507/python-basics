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

`
a = ' Hello World'
print(a.upper())
print(a.lower())
print(a.strip()) # remove whitespace from beginning and end
print(a.replace("H","j"))  # replace is case sensitive
print(a.split(",")
`
**We can combine string and number by using `format()`**
`
age =35
name = 'Amit'
txt = "My age is {} and name is {}"
print(txt.format(age, name))
`


























