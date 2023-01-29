## Python Basics - 2 🚀👩‍🚀

### - for loop 🔄

```python

# example 1
for i in range(10): # range(10) = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    print(i)

# example 2
for i in range(1, 10): # range(1, 10) = [1, 2, 3, 4, 5, 6, 7, 8, 9]
    print(i)

# example 3
for i in range(1, 10, 2): # range(1, 10, 2) = [1, 3, 5, 7, 9]
    print(i)

# example 4
for i in range(10, 0, -1): # range(10, 0, -1) = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
    print(i)

# example 5
my_dict = {"key_1": "value_1", "key_2": "value_2", "key_3": "value_3"} # dictionary
for key, value in my_dict.items():
    print(key, value)

```

### - while loop 🔁

```python
while True:
    print("Hello World")
```

### - if statement 📝

```python
i = 4
if i>5:
    print("i is greater than 5")
elif i<5:
    print("i is less than 5")
else:
    print("i is equal to 5")
```

### - Functions 📝

```python
def my_function():
    print("Hello World")
my_function()

def my_function_2(name):
    print("Hello " + name)
my_function_2("John")

def my_function_3(name="John"):
    print("Hello " + name)
my_function_3()

def my_function_4(name="John"):
    return "Hello " + name
print(my_function_4())
```

### - random module 🎲

```python
import random
random.randint(1, 10) # return a random integer between 1 and 10
random.choice([1, 2, 3, 4, 5]) # return a random element from a list
random.shuffle([1, 2, 3, 4, 5]) # shuffle a list
random.sample([1, 2, 3, 4, 5], 3) # return a list of 3 random elements from a list
random.random() # return a random float between 0 and 1
random.uniform(1, 10) # return a random float between 1 and 10
```

### - datetime module 📅

```python
import datetime
datetime.now() # return the current date and time
datetime.now().year # return the current year
datetime.now().month # return the current month
datetime.now().day # return the current day
datetime.now().hour # return the current hour
datetime.now().minute # return the current minute
datetime.now().second # return the current second
datetime.now().microsecond # return the current microsecond
datetime.now().strftime("%Y") # return the current year in string format
datetime.now().strftime("%m") # return the current month in string format
datetime.now().strftime("%d") # return the current day in string format
datetime.now().strftime("%H") # return the current hour in string format
datetime.now().strftime("%M") # return the current minute in string format
datetime.now().strftime("%S") # return the current second in string format
datetime.now().strftime("%f") # return the current microsecond in string format
datetime.now().strftime("%Y-%m-%d") # return the current date in string format
datetime.now().strftime("%H:%M:%S") # return the current time in string format
datetime.now().strftime("%Y-%m-%d %H:%M:%S") # return the current date and time in string format
datetime.now().strftime("%Y-%m-%d %H:%M:%S.%f") # return the current date and time with microsecond in string format
datetime.now().timestamp() # return the current date and time in seconds
datetime.now().timedelta(days = 1)
datetime.now().timedelta(days = -1)
datetime.now().timedelta(hours = 1)
datetime.now().timedelta(days = 10, hours = 1, minutes = 1, seconds = 1, microseconds = 1)
```

### - import local module 🌍

```python
import locale
locale.setlocale(locale.LC_ALL, 'en_US.UTF-8') # set the locale
```

### - import time module ⏰

```python
import time
time.time() # return the current time in seconds
time.localtime() # return the current time in a struct_time format
time.localtime().tm_year # return the current year
time.localtime().tm_mon # return the current month
time.localtime().tm_mday # return the current day
time.localtime().tm_hour # return the current hour
time.localtime().tm_min # return the current minute
time.localtime().tm_sec # return the current second
time.localtime().tm_wday # return the current weekday
time.localtime().tm_yday # return the current day of the year
time.localtime().tm_isdst # return the current daylight saving time flag
time.sleep(1) # sleep for 1 second
```

- Thanks for reading. If you have any questions, please feel free to ask me. I will be happy to help you. See you in the Python Basics - 2. 👋
- If you want more exercises, you can check out my Kaggle account [-Kaggle-](https://www.kaggle.com/burakbodurolu) and Python Projects account [-Python Projects-](https://github.com/burakboduroglu/Python-Projects).
