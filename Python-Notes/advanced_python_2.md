## Advanced Python - 2 🚀👩‍🚀

### - kwargs

- kwargs allows us to pass a variable number of keyword arguments to a function. We use the \*\* operator to unpack the dictionary into keyword arguments.
- kwargs is a dictionary.

```python
# Example 1
def func(**kwargs):
    print(kwargs)

func(name='name_1', age=30)
# Output -> {'name': 'name_1', 'age': 30}
```

### - args

- args allows us to pass a variable number of arguments to a function. We use the \* operator to unpack the list into positional arguments.

- args is a tuple.

```python
# Example 1
def func(*args):
    print(args)

func(1, 2, 3, 4, 5)
# Output -> (1, 2, 3, 4, 5)

# Example 2
def super_func(*args, **kwargs):
    total = 0
    for items in kwargs.values():
        total += items
    return sum(args) + total
print(super_func(1, 2, 3, 4, 5, num1=5, num2=10))
# Output -> 40
```

### - global

- global allows us to modify a global variable inside a function.

### - lambda

- lambda is a way to create an anonymous function (a function without a name).
- lambda is a one-line function.

```python
# Example 1
square = lambda num: num * num
print(square(2))
# Output -> 4

# Example 2
add = lambda a, b: a + b
print(add(2, 3))
# Output -> 5
```

### - filter

- filter is a built-in function of Python. It allows us to filter out items in an iterable (list, tuple, etc.) that don't match a certain condition.

```python
# Example 1
def check_even(num):
    return num % 2 == 0

my_nums = [1, 2, 3, 4, 5, 6]
print(list(filter(check_even, my_nums)))
# Output -> [2, 4, 6]

# Example 2
my_nums = [1, 2, 3, 4, 5, 6]
print(list(filter(lambda num: num % 2 == 0, my_nums)))
# Output -> [2, 4, 6]
```

### - map

- map is a built-in function of Python. It allows us to execute a function for each item in an iterable (list, tuple, etc.).

```python
# Example 1
def square(num): return num * num

my_nums = [1, 2, 3, 4, 5]
print(list(map(square, my_nums)))
# Output -> [1, 4, 9, 16, 25]

# Example 2
my_nums = [1, 2, 3, 4, 5]
print(list(map(lambda num: num * num, my_nums)))
# Output -> [1, 4, 9, 16, 25]

# Example 3
def splicer(mystring):
    if len(mystring) % 2 == 0:
        return 'EVEN'
    else:
        return mystring[0]

names = ['Andy', 'Eve', 'Sally']
print(list(map(splicer, names)))
# Output -> ['EVEN', 'E', 'S']


# Example 4
def check_even(num):
    return num % 2 == 0

my_nums = [1, 2, 3, 4, 5, 6]
print(list(map(lambda num: num * 2, filter(check_even, my_nums))))
# Output -> [4, 8, 12]
```

### - keyword arguments

- keyword arguments are arguments preceded by an identifier when we pass them to a function. The order of the arguments can be changed.

```python
# Example 1
def func(a, b, c):
    print(a, b, c)

func(1, 2, 3)
# Output -> 1 2 3

func(c=3, b=2, a=1)
# Output -> 1 2 3
```

### - all any

- all() returns True if all elements in an iterable are true (or if the iterable is empty).

- any() returns True if any element of an iterable is true. If the iterable is empty, it returns False.

```python
# Example 1
my_list = [True, True, True]
print(all(my_list))
# Output -> True

my_list = [True, False, True]
print(all(my_list))
# Output -> False

# Example 2
my_list = [1, 2, 3, 4, 5, 6]
print(all([num % 2 == 0 for num in my_list]))
# Output -> False
```
