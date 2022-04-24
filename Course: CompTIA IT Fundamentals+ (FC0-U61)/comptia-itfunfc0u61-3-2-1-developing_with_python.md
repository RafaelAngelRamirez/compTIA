Filename: comptia-itfunfc0u61-3-2-1-developing_with_python
Show Name: CompTIA IT Fundamentals (Exam FC0-U61)
Topic Name: Software Development
Episode Name: Developing with Python
Show Description: In this episode, Don and Ronnie demonstrate how to write an application using the Python development language. They start with a simple application and then add in elements like variables, functions and loops to create a more complex example. 

#### Developing with Python
---

**Simple hello world application**

```python
print("Hello World!")
```

**Using a variable**

```python
name = "Ronnie"
print("Hello " + name + "!")
```

**Using multiple variables**

```python
name1 = "Ronnie"
name2 = "Don"

print("Hello " + name1 + " and " + name2 + "!")
```

**Calling a function**

```python
def hello(name):
  print("Hello " + name + "!")

hello("Ronnie")
hello("Don")
```

**Using If Statements**

```python
def hello(name):
  if(name == "Ronnie"):
    print(name + " is my favorite!")
  else:
    print(name + " is super boring.")

hello("Ronnie")
hello("Don")
```

**Looping a function**

```python
def hello(name):
  if(name == "Ronnie"):
    print(name + " is my favorite!")
  else:
    print(name + " is super boring.")

loop = 0
while(loop < 6):
  hello("Ronnie")
  hello("Don")
  loop = loop + 1
```