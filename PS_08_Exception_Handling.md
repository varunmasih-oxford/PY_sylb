# Section 8. Exception Handling

## Topics
- try…except
- try…except…finally
- try…except…else
- Raising exceptions manually (`raise`)
- Creating custom exceptions
---

# 1. What is an Exception?

An **exception** is an error that occurs during the execution of a program.

### Example

```python
print(10/0)
```

Output:

```
ZeroDivisionError: division by zero
```

This error stops the program. To prevent this, we use **exception handling**.

---

# 2. try and except

The **try block** contains code that might produce an error.
The **except block** handles the error.

### Syntax

```python
try:
    # risky code
except:
    # code to handle error
```

### Example

```python
try:
    num = int(input("Enter number: "))
    result = 10 / num
    print(result)
except:
    print("An error occurred")
```

---

# 3. Handling Specific Exceptions

It is better to handle **specific exceptions** instead of a general exception.

### Example

```python
try:
    num = int(input("Enter number: "))
    result = 10 / num
    print(result)

except ZeroDivisionError:
    print("Cannot divide by zero")

except ValueError:
    print("Invalid input")
```

---

# 4. Multiple Exceptions in One Block

```python
try:
    num = int(input("Enter number: "))
    result = 10 / num
    print(result)

except (ZeroDivisionError, ValueError):
    print("Error occurred")
```

---

# 5. else Block

The **else block executes only if no exception occurs**.

```python
try:
    num = int(input("Enter number: "))
    result = 10 / num

except ZeroDivisionError:
    print("Cannot divide by zero")

else:
    print("Result:", result)
```

---

# 6. finally Block

The **finally block always executes**, whether an exception occurs or not.

Used for:

* Closing files
* Releasing resources
* Database connections

### Example

```python
try:
    file = open("data.txt", "r")
    print(file.read())

except FileNotFoundError:
    print("File not found")

finally:
    print("Execution completed")
```

---

# 7. Raising Exceptions

Python allows us to **manually raise exceptions** using `raise`.

### Example

```python
age = int(input("Enter age: "))

if age < 18:
    raise ValueError("Age must be 18 or above")

print("Access granted")
```

---

# 8. Custom Exception

We can create **our own exception classes**.

### Example

```python
class NegativeNumberError(Exception):
    pass

num = int(input("Enter number: "))

if num < 0:
    raise NegativeNumberError("Negative numbers are not allowed")
```

---

# 9. Example Program

```python
try:
    a = int(input("Enter first number: "))
    b = int(input("Enter second number: "))

    result = a / b

except ZeroDivisionError:
    print("Division by zero is not allowed")

except ValueError:
    print("Please enter valid numbers")

else:
    print("Result:", result)

finally:
    print("Program finished")
```

---

# 10. Common Python Exceptions

| Exception         | Description            |
| ----------------- | ---------------------- |
| ZeroDivisionError | Division by zero       |
| ValueError        | Invalid value          |
| TypeError         | Wrong data type        |
| IndexError        | Invalid list index     |
| KeyError          | Invalid dictionary key |
| FileNotFoundError | File not found         |
| NameError         | Variable not defined   |

---

# Best Practices

* Always catch **specific exceptions**
* Avoid using **bare except**
* Use **finally** for cleanup tasks
* Use **raise** when creating custom validations

