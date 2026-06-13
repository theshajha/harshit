# 11 — Classes & Objects (OOP)

> One line: a way to bundle data and the functions that act on it into one thing — "objects" — for code that models the real world.

## The idea
A **class** is a blueprint; an **object** is a thing made from it. A `Dog` class describes what every dog *has* (name, age — attributes) and *does* (bark — methods); each actual dog is an object (an *instance*). OOP shines when you have many things of the same kind, each with its own data. You've already used objects constantly — strings and lists are objects with methods (`"hi".upper()`).

## Quick reference

```python
class Dog:
    def __init__(self, name, age):   # the constructor — runs when you make one
        self.name = name             # 'self' = this particular dog
        self.age = age

    def bark(self):                  # a method
        return f"{self.name} says woof"

d = Dog("Rex", 3)        # make an instance
d.name                   # 'Rex'        (access an attribute)
d.bark()                 # 'Rex says woof'  (call a method)
isinstance(d, Dog)       # True
```

| Word | Means |
|------|-------|
| class | the blueprint |
| object / instance | a thing made from the class |
| attribute | data on the object (`self.name`) |
| method | a function on the object (`bark`) |
| `__init__` | the setup function, runs on creation |
| `self` | "this specific object" |

## Worked example
*(complete after the lecture)*
```python
class Counter:
    def __init__(self):
        self.count = 0
    def tick(self):
        self.count += 1
```

## Gotchas
- **`self`** is always the first parameter of a method, and you don't pass it yourself — Python does.
- Set up all your attributes in `__init__` so every object starts complete.
- Don't force OOP everywhere — for simple scripts, plain functions are often cleaner. Use classes when data + behaviour belong together.

## ✍️ Your turn
- What `self` means, in your own words:
- A small class you wrote:

## Go deeper
- CS50P — Object-Oriented Programming (Week 8)
