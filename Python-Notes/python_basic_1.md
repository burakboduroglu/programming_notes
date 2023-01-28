## Python Basics - 1 🚀👩‍🚀

#### - Data Structures 📄

```python
number_1 = 5 # integer
number_2 = 5.2 # float
string_1 = "Hello World" # string
boolean_1 = True # boolean
list_1 = [1, 2, 3, 4, 5] # list
tuple_1 = (1, 2, 3, 4, 5) # tuple
dictionary_1 = {"key_1": "value_1"} # dictionary
set_1 = {1, 2, 3, 4, 5} # set
```

#### - Operators

```python
# Arithmetic Operators
5 + 5 # 10
5 - 5 # 0
5 * 5 # 25
5 / 5 # 1.0
5 % 5 # 0
5 ** 5 # 125
5 // 5 # 1

# Comparison Operators
5 == 5 # True
5 != 5 # False
5 > 5 # False
5 < 5 # False
5 >= 5 # True
5 <= 5 # True

# Logical Operators
True and True # True
True and False # False
True or True # True
True or False # True
not True # False
not False # True
```

- ### About Lists
  It is a collection which is ordered and changeable. Allows duplicate members.

```python
list_1 = [1, 2, 3, 4, 5]
list_1.append(6) # add an element to the end of the list
list_1.insert(3, 12) # insert an element at a given position (index, element)
list_1.remove(12) # remove an element from the list
list_1.pop() # remove the last element from the list
list_1.pop(3) # remove the element at the specified position
list_1.clear() # remove all elements from the list
list_1.index(3) # return the index of the first element with the specified value
list_1.count(3) # return the number of elements with the specified value
list_1.sort() # sort the list
list_1.reverse() # reverse the list
list_1.copy() # copy the list
```

- ### About Tuples
  It is a collection which is ordered and unchangeable. Allows duplicate members.

```python
tuple_1 = (1, 2, 3, 4, 5)
tuple_1.count(3) # return the number of elements with the specified value
tuple_1.index(3) # return the index of the first element with the specified value
```

- ### About Sets
  It is a collection which is unordered and unindexed. No duplicate members.

```python
set_1 = {1, 2, 3, 4, 5}
set_1.add(6) # add an element to the set
set_1.update([7, 8, 9]) # add multiple elements to the set
set_1.remove(9) # remove an element from the set
set_1.discard(9) # remove an element from the set if it is a member
set_1.pop() # remove an element from the set
set_1.clear() # remove all elements from the set
set_1.copy() # copy the set
```

- ### About Dictionaries 🔑📔
  It is a collection which is unordered, changeable and indexed. No duplicate members.

```python
dictionary_1 = {"key_1": "value_1"}
dictionary_1["key_2"] = "value_2" # add an element to the dictionary
dictionary_1.pop("key_2") # remove an element from the dictionary
dictionary_1.popitem() # remove the last inserted element from the dictionary
dictionary_1.clear() # remove all elements from the dictionary
dictionary_1.copy() # copy the dictionary
dictionary_1.keys() # return a list of all the keys in the dictionary
dictionary_1.values() # return a list of all the values in the dictionary
dictionary_1.items() # return a list of tuples containing the key-value pairs
dictionary_1.get("key_1") # return the value of the specified key
dictionary_1.update({"key_3": "value_3"}) # update the dictionary with the specified key-value pairs
dictionary_1.setdefault("key_4", "value_4") # return the value of the specified key. If the key does not exist: insert the key, with the specified value
```

- ### About Strings
  It is a collection of characters.

```python
string_1 = "Hello World"
string_1.capitalize() # capitalize the first letter of the string
string_1.lower() # convert the string to lower case
string_1.upper() # convert the string to upper case
string_1.isdigit() # check if the string is a digit
string_1.isalpha() # check if the string is an alphabet
string_1.isalnum() # check if the string is an alphanumeric
string_1.islower() # check if the string is in lower case
string_1.isupper() # check if the string is in upper case
string_1.strip() # remove whitespaces from the beginning and the end of the string
string_1.strip('*') # remove the specified characters from the beginning and the end of the string
string_1.replace("Hello", "Hi") # replace a string with another string
string_1.split() # split the string into substrings if it finds instances of the separator
string_1.split(',') # split the string into substrings if it finds instances of the separator
string_1.join(["Hello", "World"]) # join the elements of an iterable to the end of the string
string_1.find("World") # search the string for a specified value and returns the position of where it was found
string_1.index("World") # search the string for a specified value and returns the position of where it was found
string_1.startswith("Hello") # check if the string starts with a specified value
string_1.endswith("World") # check if the string ends with a specified value
string_1.count("l") # return the number of times a specified value occurs in a string
string_1.format() # format specified values in a string
```

- Thanks for reading. If you have any questions, please feel free to ask me. I will be happy to help you. See you in the Python Basics - 2. 👋
- If you want more exercises, you can check out my Kaggle account [-Kaggle-](https://www.kaggle.com/burakbodurolu) and Python Projects account [-Python Projects-](https://github.com/burakboduroglu/Python-Projects).
