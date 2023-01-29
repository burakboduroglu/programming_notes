## Python Basics - 3 🚀👩‍🚀

### - subprocessing 📄

```python
import subprocess

subprocess.call("calc.exe") # it will open the calculator
```

### - try except finally

```python
try: # try to execute this block of code
    print("Hello World")
except: # if there is an error, execute this block of code
    print("Something went wrong")
else: # if there is no error, execute this block of code
    print("Nothing went wrong")
finally: # this block of code will be executed no matter if there is an error or not
    print("The 'try except' is finished")
```

### - raise

```python
x = -1
if x < 0:
    raise Exception("Sorry, no numbers below zero") # it will raise an error
```

### - assert

- assert is used to test if a condition in your code returns True, if not, the program will raise an AssertionError.

```python
x = "hello"
assert x == "hello" # it will return nothing
assert x == "goodbye" # it will raise an AssertionError
```

### - error types

- SyntaxError
- NameError
- TypeError
- IndexError
- ValueError
- KeyError
- ModuleNotFoundError
- ImportError
- AttributeError

### - file processing

```python
# open a file
file = open("file.txt", "r") # "r" means read only

# read a file
print(file.read()) # read the whole file

# read a file line by line
print(file.readline()) # read the first line

# read all lines
print(file.readlines()) # read all lines

# write to a file
file = open("file.txt", "w") # "w" means write only
file.write("Hello World")

# append to a file
file = open("file.txt", "a") # "a" means append only
file.write("Hello World")

# close a file
file.close()
```

### - codecs

```python
import codecs

# open a file
file = codecs.open("file.txt", "r", "utf-8") # "utf-8" means unicode

# read a file
print(file.read()) # read the whole file


# with statement (it will close the file automatically)
with codecs.open("file.txt", "r", "utf-8") as file:
    print(file.read()) # read the whole file
```

### - seek

```python
# open a file
file = open("file.txt", "r")

# seek to a position
file.seek(0) # seek to the beginning of the file

```

### - insert file

```python
# open a file
file = open("file.txt", "r")
file.insert(0, "Hello World") # it will insert "Hello World" to the beginning of the file
```

### - writelines

```python
# open a file
file = open("file.txt", "r")

# writelines
file = open("file.txt", "r")
file2 = open("file2.txt", "w")
file2.writelines(file.readlines()) # it will write all lines to the file
```

### - delete file

```python
import os

# delete a file
os.remove("file.txt")
```

- Thanks for reading. If you have any questions, please feel free to ask me. I will be happy to help you. See you in the Python Basics - 2. 👋
- If you want more exercises, you can check out my Kaggle account [-Kaggle-](https://www.kaggle.com/burakbodurolu) and Python Projects account [-Python Projects-](https://github.com/burakboduroglu/Python-Projects).
