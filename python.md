# Python

Welcome to the **Python Wiki**! This is a comprehensive resource for developers working with Python, offering insights, tips, and examples to help you harness the full power of this versatile programming language.  

## Description  

Python is a high-level, interpreted programming language known for its readability and flexibility. It is widely used in web development, data science, machine learning, automation, and more. With an extensive ecosystem of libraries and frameworks, Python enables rapid development and scalable solutions.  

This wiki serves as a central hub to explore Python's features, understand its capabilities, and access helpful resources to enhance your projects.  

## Useful Links  

- [Official Python Documentation](https://docs.python.org/3/)  
- [PyPI - Python Package Index](https://pypi.org/)  
- [Python GitHub Repository](https://github.com/python/cpython)  
- [Python Style Guide (PEP 8)](https://peps.python.org/pep-0008/)  
- [Interactive Python Tutorials](https://www.learnpython.org/)  

## Table of Contents  

- [Description](#description)  
- [Useful Links](#useful-links)  
- [Python Versions](#python-versions)  
- [Basic Code Examples](#basic-code-examples)  

## Python Versions  

Python has evolved significantly since its creation. Below are some key milestones:  

- **Python 2.x**  
  Introduced a wide range of libraries but officially deprecated in 2020.  

- **Python 3.0**  
  Released in 2008, introduced major improvements like Unicode support and better syntax, breaking backward compatibility with Python 2.  

- **Python 3.6**  
  Added f-strings for easier string formatting and type hints for better code clarity.  

- **Python 3.9**  
  Introduced dictionary union operators (`|`), type hinting for built-in types, and more.  

- **Python 3.11**  
  Released in 2022, includes faster execution and improved error messages.  

For a complete history of Python versions, visit the [Python Release Notes](https://docs.python.org/3/whatsnew/).  

## Basic Code Examples  

Here are some practical Python examples to get you started:  

**"Hello, World" Example**  
```python
print("Hello, World!")
```

**Reading a File**  
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

**Using a For Loop**  
```python
for i in range(5):
    print(f"Iteration {i}")
```

**Simple Function**  
```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))
```

**Fetching Data from a Web API**  
```python
import requests

response = requests.get("https://api.github.com")
if response.status_code == 200:
    print("API data:", response.json())
else:
    print("Failed to fetch data")
```

**Basic Object-Oriented Programming**  
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"{self.name} makes a sound.")

dog = Animal("Dog")
dog.speak()
```

