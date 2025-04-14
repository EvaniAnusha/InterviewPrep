# Language basics for DSA

## List:
```python
nums = [1,2,3]
```

### Common methods
```python
nums.index(1)      # Find index
nums.append(1)     # Add to end
nums.pop()         # Remove & return last element
nums.sort()        # In-place sort (TimSort: O(n log n))
nums.reverse()     # In-place reverse
nums.copy()        # Return shallow copy
```

### List Slicing
```python
nums[-1]    # Last item
nums[::-1]  # Reverse list
nums[1:]    # Everything after index 1
nums[:3]    # First three elements
nums[1:3]   # Second two elements
nums[start:stop:step]  # Generic slice syntax
```

## Dict
```python
d = {'a':1, 'b':2}
```
### Essential Operations
```python
d.get('key', default)     # Safe access with default

d.items()                 # Key-value pairs
d.keys()                  # Just keys
d.values()                # Just values

d.pop(key, default)       # Remove and return value
```



## Set
```python
s = {1,2,3}
```
### Common Operations
```python
s.add(4)             # Add element
s.remove(4)          # Remove (raises error if missing)
```

### Set Operations
```python
a.union(b)           # Elements in a OR b
a.intersection(b)    # Elements in a AND b
a.difference(b)      # Elements in a but NOT in b

a.issubset(b)        # True if all elements of a are in b
a.issuperset(b)      # True if all elements of b are in a
```

## String 
```python
s = "hello world"
```
### Essential Methods
```python
s.split()            # Split on whitespace
s.split(',')         # Split on comma

s.strip()            # Remove leading/trailing whitespace

s.lower()            # Convert to lowercase
s.upper()            # Convert to uppercase

s.isalpha()          # Check if alphabetic
s.isdigit()          # Check if all digits

s.find('sub')        # Index of substring (-1 if not found)
s.replace('old', 'new')  # Replace all occurrences
```
## Definitions: `isalpha() & isdigit()` 
```python
def isalpha(val):
	if (ord('a') <= ord(val) && ord(val) <= ord('a')+25) || (ord('A') <= ord(val) && ord(val) <= ord('A')+25) :
		return True


def isdigit(val):
	if (ord('0') <= ord(val) && ord(val) <= ord('9')):
		return True 
```

### Join Lists

```python
''.join(['a','b'])   # Concatenate list elements
```

## ASCII Conversion
```python
ord('a')             # Char to ASCII (97)
chr(97)              # ASCII to char ('a')
```

### enumerate function
```python
chars = ['a', 'b', 'c', 'd', 'e']
for ind, c in enumerate(chars):
  print("ind:", ind, "character:", c)

```

### zip function
```python 
nums = [1, 2, 3, 4, 5, 6]
chars = ['a', 'b', 'c', 'd', 'e']

# print tuples
for _ in zip(nums, chars):
    print(_)				

# destructure the tuples 
for nums, chars in zip(nums, chars):
    print(nums, chars)
```	


# Convert to list of integers
```python 
test = 5
inp_list = []
for i in range(test):
	inp_list.append(input())

inp_list = ['10', '20', '30', '40']

# convert string to mapobject (int)
# map(int, inp_list)

# convert the mapobject (int) to list
# list(map(int, inp_list))

nums_inp_list = list(map(int, inp_list))

# Output: [10, 20, 30, 40]
```

```python
# convert strings to list of ints
list(map(int, input('Enter the numbers').split() ))

# It's also same as above line of code
[int(x) for x in input("Enter two numbers: ").split()]
```



# Type Conversion
```python
int('42')            # String to int
str(42)              # Int to string
list('abc')          # String to list
''.join(['a','b'])   # List to string
set([1,2,2])         # List to set
```

# Math
```python
abs(-5)              # Absolute value
pow(2, 3)            # Power
round(3.14159, 2)    # Round to decimals
```
