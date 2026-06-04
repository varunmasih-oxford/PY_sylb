# Section 16. Object-Oriented Programming (OOP)

## Topics
- Classes and objects
- Constructors (`__init__`)
- Instance and class variables
- Methods
- Inheritance
- Polymorphism
- Encapsulation
- Magic (dunder) methods (`__str__`, `__len__`, etc.)
# Python OOP Concepts (Simple Explanation)

---

# 1. Classes and Objects

A **class** is a blueprint.
An **object** is a real item created from the class.

### Example:

```python
class Student:
    name = "Varun"

# object creation
s1 = Student()

print(s1.name)
```

### Output:

```python
Varun
```

### Real Life:

* Class = Car design
* Object = Actual car

---

# 2. Constructor (`__init__`)

`__init__` runs automatically when an object is created.

Used to give values to objects.

### Example:

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

s1 = Student("Varun", 22)

print(s1.name)
print(s1.age)
```

### Output:

```python
Varun
22
```

---

# 3. Instance Variables and Class Variables

## Instance Variable

Different for every object.

### Example:

```python
class Student:
    def __init__(self, name):
        self.name = name

s1 = Student("Varun")
s2 = Student("Aman")

print(s1.name)
print(s2.name)
```

### Output:

```python
Varun
Aman
```

---

## Class Variable

Common for all objects.

### Example:

```python
class Student:
    school = "ABC School"   # class variable

    def __init__(self, name):
        self.name = name

s1 = Student("Varun")
s2 = Student("Aman")

print(s1.school)
print(s2.school)
```

### Output:

```python
ABC School
ABC School
```

---

# 4. Methods

Functions created inside a class are called methods.

### Example:

```python
class Student:
    def __init__(self, name):
        self.name = name

    def show(self):
        print("Student Name:", self.name)

s1 = Student("Varun")
s1.show()
```

### Output:

```python
Student Name: Varun
```

---

# 5. Inheritance

One class can use properties of another class.

### Example:

```python
class Parent:
    def house(self):
        print("Parent's House")

class Child(Parent):
    pass

c1 = Child()
c1.house()
```

### Output:

```python
Parent's House
```

### Real Life:

Child inherits family properties.

---

# 6. Polymorphism

Same method name behaves differently.

### Example:

```python
class Dog:
    def sound(self):
        print("Dog barks")

class Cat:
    def sound(self):
        print("Cat meows")

d = Dog()
c = Cat()

d.sound()
c.sound()
```

### Output:

```python
Dog barks
Cat meows
```

---

# 7. Encapsulation

Hiding data from direct access.

### Example:

```python
class Bank:
    def __init__(self):
        self.__balance = 5000   # private variable

    def show_balance(self):
        print(self.__balance)

b1 = Bank()
b1.show_balance()
```

### Output:

```python
5000
```

### Wrong Access:

```python
print(b1.__balance)
```

### Output:

```python
Error
```

---

# 8. Magic (Dunder) Methods

Special methods with double underscores.

---

## `__str__`

Controls object printing.

### Example:

```python
class Student:
    def __init__(self, name):
        self.name = name

    def __str__(self):
        return self.name

s1 = Student("Varun")

print(s1)
```

### Output:

```python
Varun
```

---

## `__len__`

Controls `len()` function.

### Example:

```python
class Students:
    def __len__(self):
        return 5

s1 = Students()

print(len(s1))
```

### Output:

```python
5
```
