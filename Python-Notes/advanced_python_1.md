## Advanced Python - 1 🚀👩‍🚀

### - Enumerate

- Enumerate is a built-in function of Python. It allows us to loop over something and have an automatic counter.

```python
# Example 1
for i, char in enumerate('Hello'):
    print(i, char)

# Output -> 0 H 1 e 2 l 3 l 4 o

# Example 2
for i, char in enumerate(list(range(100))):
    if char == 50:
        print(f'The index of 50 is: {i}')
```

### - Zip

- Zip is a built-in function of Python. It allows us to loop over two lists at the same time.

```python
# Example 1
list1 = [1, 2, 3]
list2 = [10, 20, 30]

for item in zip(list1, list2):
    print(item)
# Output -> (1, 10) (2, 20) (3, 30)

# Example 2
list1 = [1, 2, 3]
list2 = [10, 20, 30, 40, 50]
list3 = ['a', 'b', 'c', 'd', 'e']

for item in zip(list1, list2, list3):
    print(item)
# Output -> (1, 10, 'a') (2, 20, 'b') (3, 30, 'c')

# Example 3
list1 = [1, 2, 3]
list2 = [10, 20, 30, 40, 50]
list3 = ['a', 'b', 'c', 'd', 'e']

for a, b, c in zip(list1, list2, list3):
    print(a, b, c)
# Output -> 1 10 a 2 20 b 3 30 c

# Example 4
list1 = [1, 2, 3]
list2 = [10, 20, 30, 40, 50]
list3 = ['a', 'b', 'c', 'd', 'e']

print(list(zip(list1, list2, list3)))
# Output -> [(1, 10, 'a'), (2, 20, 'b'), (3, 30, 'c')]
```

### - Unzip

- Unzip is a built-in function of Python. It allows us to unzip a list.

```python
# Example 1
list1 = [1, 2, 3]
list2 = [10, 20, 30]

unzipped = list(zip(list1, list2))
print(unzipped)
# Output -> [(1, 10), (2, 20), (3, 30)]
```

### - List Comprehension

- List comprehension is a way to create a list using for loop in a single line.

```python
# Example 1
my_list = [char for char in 'hello']
print(my_list)
# Output -> ['h', 'e', 'l', 'l', 'o']

# Example 2
my_list = [num for num in range(0, 8)]
print(my_list)
# Output -> [0, 1, 2, 3, 4, 5, 6, 7]

# Example 3
my_list = [num**2 for num in range(0, 5)]
print(my_list)
# Output -> [0, 1, 4, 9, 16]

# Example 4
my_list = [num**2 for num in range(0, 5) if num % 2 == 0]
print(my_list)
# Output -> [0, 4, 16]

# Example 5
my_list = [x*y for x in [2, 4, 6] for y in [1, 10, 1000]]
print(my_list)
# Output -> [2, 20, 2000, 4, 40, 4000, 6, 60, 6000]

# Example 6
my_list = [x*y for x in [2, 4, 6] for y in [1, 10, 1000] if x*y > 50]
print(my_list)
# Output -> [60, 6000]

# Example 7
my_list = [x if x % 2 == 0 else 'ODD' for x in range(0, 10)]
print(my_list)
# Output -> [0, 'ODD', 2, 'ODD', 4, 'ODD', 6, 'ODD', 8, 'ODD']
```

### - Dictionary Comprehension

- Dictionary comprehension is a way to create a dictionary using for loop in a single line.

```python
# Example 1
simple_dict = {
    'a': 1,
    'b': 2
}

my_dict = {key: value**2 for key, value in simple_dict.items()}
print(my_dict)
# Output -> {'a': 1, 'b': 4}
```

### - Set Comprehension

- Set comprehension is a way to create a set using for loop in a single line.

```python
# Example 1
simple_set = {1, 2, 3}

my_set = {num for num in simple_set}
print(my_set)
# Output -> {1, 2, 3}
```
