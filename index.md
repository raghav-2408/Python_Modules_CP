# Useful modules for CP (Python) :

`code`
```python
from collections import Counter

# Counting occurrences of elements in a list
data = [1, 2, 3, 1, 2, 3, 4, 5, 1, 2]
res = Counter(data)
for key, value in res.items():
    print(f"{key} repeated {value} times")
print(res)

```
`Output`

1 repeated 3 times <br>
2 repeated 3 times <br>
3 repeated 2 times <br>
4 repeated 1 times <br>
5 repeated 1 times <br> 
Counter({1: 3, 2: 3, 3: 2, 4: 1, 5: 1})
<hr>

`code`
```python
from itertools import combinations

# Generating combinations of elements in a list
data = [1, 2, 3]
comb = combinations(data, 2)
print(list(comb))
```
`Ouput`

[(1, 2), (1, 3), (2, 3)]
<hr>

`code`
```python
from functools import reduce

# Using reduce to find the product of elements in a list
data = [2, 3, 4, 5] # 2 * 3 * 4 * 5 = 120
product = reduce(lambda x, y: x * y, data)
print(product)
```
`Output`

120 

<hr>

`code`
```python
from contextlib import contextmanager

# Creating a simple context manager
@contextmanager
def my_context():
    print("Entering the context")
    yield
    print("Exiting the context")

with my_context():
    print("Inside the context")
```
`Output`

Entering the context <br>
Inside the context <br>
Exiting the context <br>
<hr>

`code`
```python
from operator import itemgetter

# Sorting a list of tuples by the second element
data = [(1, 5), (3, 2), (2, 8)]
sorted_data = sorted(data, key=itemgetter(1))
print(sorted_data)
```
`Output`

[ (3, 2), (1, 5), (2, 8) ]
<hr>

`code`
```python
from fractions import Fraction

# Performing precise arithmetic with fractions
# result = Fraction(1, 3) + Fraction(1, 6)
result = Fraction(1, 3)
print(result)
```
`Output`

1/3
<hr>

`code`
```python
import heapq

# Using heapq to find the three smallest elements in a list
# Can adjust based on our needs
data = [5, 3, 9, 1, 7] 
smallest_three = heapq.nsmallest(3, data)
print(smallest_three)
```
`Output`

[1, 3, 5]
<hr>

`code`
```python
 import sys

# Faster input reading
data = sys.stdin.readline().strip() # hey
print(data)
```
`Output`

hey
<hr>

`code`
```python
# Initial value of num
num = 5

# Bit position to check, set, and toggle
bit_position = 1

# Checking if a bit is set
if (num & (1 << bit_position)) != 0:
    print(f"Bit at position {bit_position} is set")
else:
    print(f"Bit at position {bit_position} is not set")

# Setting a bit
num |= (1 << bit_position)
print(f"After setting bit at position {bit_position}, num is now: {num}")

# Toggling a bit
num ^= (1 << bit_position)
print(f"After toggling bit at position {bit_position}, num is now: {num}")

```
`Output`

Bit at position 1 is not set  <br>
After setting bit at position 1, num is now: 7 <br>
After toggling bit at position 1, num is now: 5 <br>
<hr>

`code`
```python
# Calculating a^b % m efficiently
a = 4
b = 2
m = 5
result = pow(a, b, m)
print(result)
```
`Output`

1
<hr>

`code`
```python
# Generate the Cartesian product and combinations, respectively.
# Adjust based on the condition
from itertools import product, combinations

cartesian = list(product([1, 2], repeat=2))
combos = list(combinations([1, 2, 3], 2))

print("Product : ", cartesian)
print("Combinations : ", combos)
```
`Output`

Product : [ (1, 1), (1, 2), (2, 1), (2, 2) ] <br>
Combinations :  [ (1, 2), (1, 3), (2, 3) ] <br>
<hr>

`code`
```python
# Useful for date and time manipulation.

from datetime import datetime, timedelta

current_time = datetime.now()
future_time = current_time + timedelta(days=7)

print(current_time)
print(future_time)
```
`Output`
2023-11-13 10:28:02.020133 <br>
2023-11-20 10:28:02.020133 <br>

<hr>

`code`
```python
# Useful for checking if two strings are anagrams.
from collections import Counter

str1 = "listen"
str2 = "silent"
is_anagram = Counter(str1) == Counter(str2)
print(is_anagram)
```
`Output`

True
<hr>

`code`
```python
# Finding the longest common prefix among a list of strings.

def longest_common_prefix(strs):
    if not strs:
        return ""
    prefix = strs[0]
    for string in strs[1:]:
        i = 0
        while i < len(prefix) and i < len(string) and prefix[i] == string[i]:
            i += 1
        prefix = prefix[:i]
    return prefix
```

`Output`

Self Explanatory
<hr>

`code`
```python
#Counts the occurrences of a substring in a string.

s = "ababab"
count = s.count("ab")
print(count)
```
`Output`

3
<hr>

`code`
```python
# enumerate()
# Provides both the index and the value when iterating over a sequence.

items = ['a', 'b', 'c']

for index, value in enumerate(items):
    print(f"Index: {index}, Value: {value}")
```
`Output`

Index: 0, Value: a <br>
Index: 1, Value: b <br>
Index: 2, Value: c <br>

<hr>

`code`
```python
# XOR is often used to find the single non-duplicated element.

nums = [2, 3, 2, 4, 4]

# Finding the single non-duplicated element
result = 0
for num in nums:
    result ^= num
print(result)
```
`Output`

3
<hr>

`code`
```python
''' Left Shift (<<) and Right Shift (>>):
Use Case: Multiplication and Division by Powers of 2
Efficient multiplication and division by 2, 4, 8, etc. '''

num = 4
# Multiplying by 2
multiplied_num = num << 1

# Dividing by 2
divided_num = num >> 1

print(multiplied_num)
print(divided_num)
```
`Output`

8
2
<hr>

`code`
```python
# Use Case: Counting the Number of Set Bits (1s) in an Integer
# Counting set bits
count = 0
while num:
    num &= num - 1
    count += 1
```
`Output`

Self Explanatory
<hr>

`code`
```python
# Use Case: Determining if a Number is a Power of 2
num = 8
is_power_of_two = (num & (num - 1)) == 0
print(is_power_of_two)
```
`Output`

True
<hr>

`code`
```python
# Use Case: Determining if a Number is Odd or Even
# 0 for even and 1 for odd.
num = 3
is_odd = num & 1
print(is_odd)
```
`Output`

1
<hr>

`code`
```python
# Use Case: Finding the Missing Number in an Array

nums = [3, 0, 1]
result = len(nums)
for i, num in enumerate(nums):
    result ^= i ^ num
print(result)
```
`Output`

2
<hr>
