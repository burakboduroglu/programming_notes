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
finally: # this block of code will be executed no matter if there is an error or not
    print("The 'try except' is finished")
```

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
