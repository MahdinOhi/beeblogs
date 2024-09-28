---
title: Python Cheatsheet
author: Mahdin Ohi
pubDatetime: 2024-09-24T09:00:00
slug: python-cheatsheet
featured: false
draft: false
tags:
  - python
  - cheatsheet
description: This Python cheatsheet offers a quick reference to essential syntax and commands, perfect for both beginners and experienced developers. Enhance your coding efficiency and master Python with this concise guide.
---

![](https://ideogram.ai/assets/image/lossless/response/m1cgxVEbRai5munG8qMPxA)

This Python cheatsheet is your go-to reference for quick programming tips, whether you're just starting out or a seasoned developer. Covering key topics, it helps you code efficiently and boost your Python skills with ease. Dive into Python confidently and streamline your workflow with this handy guide.

01 — **_Data Types_**

```Python
int_num = 42  
float_num = 3.14  
string_var = "Hello, Python!"  
bool_var = True
```

02 — **_Variables and Assignment_**

```python
x = 10  
y = "Python"
```

03 — **_Lists & Tuples_**

```python
my_list = \[1, 2, 3, "Python"\]  
my_tuple = (1, 2, 3, "Tuple")
```

04 — **_Dictionaries_**

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'Pythonville'}
```

05 — **_Control Flow_**

```python
if x > 0:  
    print("Positive")  
elif x == 0:  
    print("Zero")  
else:  
    print("Negative")  
for item in my_list:  
    print(item)  
while condition: 
```

06 — **_Functions_**

```python
def greet(name="User"):  
    return f"Hello, {name}!"  
result = greet("John")
```

07 — **_Classes & Objects_**

```python
class Dog:  
    def \_\_init\_\_(self, name):  
        self.name = name  
def bark(self):  
        print("Woof!")  
my_dog = Dog("Buddy")  
my_dog.bark()
```

08 — **_File Handling_**

```python
with open("file.txt", "r") as file:  
    content = file.read()  
with open("new_file.txt", "w") as new_file:  
    new_file.write("Hello, Python!")
```

09 — **_Exception Handling_**

```python
try:  
    result = 10 / 0  
except ZeroDivisionError:  
    print("Cannot divide by zero!")  
finally:  
    print("Execution completed.")
```

10 — **_Libraries & Modules_**

```python
import math  
from datetime import datetime  
result = math.sqrt(25)  
current_time = datetime.now()
```

11 — **_List Comprehensions_**

```python
squares = \[x**2 for x in range(5)\]
```

12 — **_Lambda Functions_**

```python
add = lambda x, y: x + y  
result = add(2, 3)
```

13 — **_Virtual Environment_**

```python
  
python -m venv myenv  
  
source myenv/bin/activate    
myenv\\Scripts\\activate    
  
deactivate
```

14 — **_Package Management_**

```python
  
pip install package_name  
  
pip list  
  
pip freeze > requirements.txt  
  
pip install -r requirements.txt
```

15 — **_Working with JSON_**

```python
import json  
  
json_data = json.dumps({"name": "John", "age": 25})  
  
python\_obj = json.loads(json\_data)
```

16 — **_Regular Expressions_**

```python
import re  
pattern = r'\\d+'    
result = re.findall(pattern, "There are 42 apples and 123 oranges.")
```

17 — **_Working with Dates_**

```python
from datetime import datetime, timedelta  
current_date = datetime.now()  
future_date = current_date + timedelta(days=7)
```

18 — **_List Manipulations_**

```python
numbers = \[1, 2, 3, 4, 5\]  
  
evens = list(filter(lambda x: x % 2 == 0, numbers))  
  
squared = list(map(lambda x: x**2, numbers))  
  
from functools import reduce  
product = reduce(lambda x, y: x * y, numbers)
```

19 — **_Dictionary Manipulations_**

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}  
  
value = my_dict.get('d', 0)  
  
squared_dict = {key: value**2 for key, value in my_dict.items()}
```

20 — **_Concurrency with Threading_**

```python
import threading  
def print_numbers():  
    for i in range(5):  
        print(i)  
thread = threading.Thread(target=print_numbers)  
thread.start()
```

21 — **_Concurrency with Asyncio_**

```python
import asyncio  
async def print_numbers():  
    for i in range(5):  
        print(i)  
        await asyncio.sleep(1)  
asyncio.run(print_numbers())
```

22 — **_Web Scraping with Beautiful Soup_**

```python
from bs4 import BeautifulSoup  
import requests  
url = "https://example.com"  
response = requests.get(url)  
soup = BeautifulSoup(response.text,   
title = soup.title.text
```

23 — **_RESTful API with Flask_**

```python
from flask import Flask, jsonify, request  
app = Flask(\_\_name\_\_)  
@app.route('/api/data', methods=\['GET'\])  
def get_data():  
    data = {'key': 'value'}  
    return jsonify(data)  
if \_\_name\_\_ == '\_\_main\_\_':  
    app.run(debug=True)
```

24 — **_Unit Testing with unittest_**

```python
import unittest  
def add(x, y):  
    return x + y  
class TestAddition(unittest.TestCase):  
    def test\_add\_positive_numbers(self):  
        self.assertEqual(add(2, 3), 5)  
if \_\_name\_\_ == '\_\_main\_\_':  
    unittest.main()
```

25 — **_Database Interaction with SQLite_**

```python
import sqlite3  
conn = sqlite3.connect('example.db')  
cursor = conn.cursor()  
\# Execute SQL query  
cursor.execute('CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, name TEXT)')  
\# Commit changes  
conn.commit()  
\# Close connection  
conn.close()
```

26 — **_File Handling_**

```python
  
with open('example.txt', 'w') as file:  
    file.write('Hello, Python!')  
  
with open('example.txt', 'r') as file:  
    content = file.read()
```

27 — **_Error Handling_**

```python
try:  
    result = 10 / 0  
except ZeroDivisionError as e:  
    print(f"Error: {e}")  
except Exception as e:  
    print(f"Unexpected Error: {e}")  
else:  
    print("No errors occurred.")  
finally:  
    print("This block always executes.")
```

28 — **_Working with JSON_**

```python
import json  
data = {'name': 'John', 'age': 30}  
\# Convert Python object to JSON  
json_data = json.dumps(data)  
\# Convert JSON to Python object  
python\_object = json.loads(json\_data)
```

29 — **_Python Decorators_**

```python
def decorator(func):  
    def wrapper():  
        print("Before function execution")  
        func()  
        print("After function execution")  
    return wrapper  
@decorator  
def my_function():  
    print("Inside the function")  
my_function()
```

30 — **_Working with Enums_**

```python
from enum import Enum  
class Color(Enum):  
    RED = 1  
    GREEN = 2  
    BLUE = 3  
print(Color.RED)
```

31 — **_Working with Sets_**

```python
set1 = {1, 2, 3}  
set2 = {3, 4, 5}  
  
union_set = set1 | set2  
  
intersection_set = set1 & set2  
  
difference_set = set1 - set2
```

32 — **_List Comprehensions_**

```python
numbers = \[1, 2, 3, 4, 5\]  
  
squares = \[x**2 for x in numbers if x % 2 == 0\]
```

33 — **_Lambda Functions_**

```python
add = lambda x, y: x + y  
result = add(3, 5)
```

34 — **_Threading with Concurrent.futures_**

```python
from concurrent.futures import ThreadPoolExecutor  
def square(x):  
    return x**2  
with ThreadPoolExecutor() as executor:  
    results = executor.map(square, \[1, 2, 3, 4, 5\])
```

35 — **_Internationalization (i18n) with gettext_**

```python
import gettext  
  
lang = 'en_US'  
_ = gettext.translation('messages', localedir='locale', languages=\[lang\]).gettext  
print(_("Hello, World!"))
```

36 — **_Virtual Environment_**

```python
  
python -m venv myenv  
  
source myenv/bin/activate    
myenv\\Scripts\\activate    
  
deactivate
```

37 — **_Working with Dates_**

```python
from datetime import datetime, timedelta  
now = datetime.now()  
  
formatted_date = now.strftime('%Y-%m-%d %H:%M:%S')  
  
future_date = now + timedelta(days=7)
```

38 — **_Working with Dictionaries_**

```python
my_dict = {'name': 'John', 'age': 30}  
  
age = my_dict.get('age', 25)  
  
for key, value in my_dict.items():  
    print(f"{key}: {value}")
```

39 — **_Regular Expressions_**

```python
import re  
text = "Hello, 123 World!"  
  
numbers = re.findall(r'\\d+', text)
```

40 — **_Working with Generators_**

```python
def square_numbers(n):  
    for i in range(n):  
        yield i**2  
squares = square_numbers(5)
```

41 — **_Database Interaction with SQLite_**

```python
import sqlite3  
\# Connect to SQLite database  
conn = sqlite3.connect('mydatabase.db')  
cursor = conn.cursor()  
\# Execute SQL query  
cursor.execute('SELECT * FROM mytable')
```

42 — **_Working with ZIP Files_**

```python
import zipfile  
with zipfile.ZipFile('archive.zip', 'w') as myzip:  
    myzip.write('file.txt')  
with zipfile.ZipFile('archive.zip', 'r') as myzip:  
    myzip.extractall('extracted')
```

43 — **_Web Scraping with requests and BeautifulSoup_**

```python
import requests  
from bs4 import BeautifulSoup  
url = 'https://example.com'  
response = requests.get(url)  
soup = BeautifulSoup(response.text, 'html.parser')  
  
title = soup.title.text
```

44 — **_Sending Email with smtplib_**

```python
import smtplib  
from email.mime.text import MIMEText  
  
server = smtplib.SMTP('smtp.gmail.com', 587)  
server.starttls()  
  
server.login('your_email@gmail.com', 'your_password')  
  
msg = MIMEText('Hello, Python!')  
msg\['Subject'\] = 'Python Email'  
server.sendmail('your_email@gmail.com', 'recipient@example.com', msg.as_string())
```

45 — **_Working with JSON Files_**

```python
import json  
data = {'name': 'John', 'age': 30}  
  
with open('data.json', 'w') as json_file:  
    json.dump(data, json_file)  
  
with open('data.json', 'r') as json_file:  
    loaded\_data = json.load(json\_file)  

```
