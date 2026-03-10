# Session 13 File Handling 

# 1. Opening a File

Python uses the **`open()`** function to open a file.

### Syntax

```python
file_object = open("filename", "mode")
```

### Common File Modes

| Mode | Description                                               |
| ---- | --------------------------------------------------------- |
| r    | Read file (default mode)                                  |
| w    | Write file (creates new file or overwrites existing file) |
| a    | Append data to file                                       |
| x    | Create new file (gives error if file already exists)      |
| rb   | Read binary file                                          |
| wb   | Write binary file                                         |

### Example

```python
file = open("data.txt", "r")
```

---

# 2. Reading a File

## read()

Reads the **entire file content**.

```python
file = open("data.txt", "r")
data = file.read()
print(data)
file.close()
```

---

## readline()

Reads **one line at a time**.

```python
file = open("data.txt", "r")
line = file.readline()
print(line)
file.close()
```

---

## readlines()

Reads **all lines and stores them in a list**.

```python
file = open("data.txt", "r")
lines = file.readlines()
print(lines)
file.close()
```

---

# 3. Writing to a File

The **write()** method is used to write data into a file.

```python
file = open("data.txt", "w")
file.write("Hello Python")
file.close()
```

⚠ Note: **`w` mode overwrites existing file content.**

---

# 4. Appending Data

Append mode adds new data **without removing existing content**.

```python
file = open("data.txt", "a")
file.write("\nNew Line Added")
file.close()
```

---

# 5. Using the `with` Statement (Best Practice)

Using **with** automatically closes the file after execution.

```python
with open("data.txt", "r") as file:
    data = file.read()
    print(data)
```

Advantages:

* No need to manually close the file
* Safer and cleaner code

---

# 6. Checking if a File Exists

```python
import os

if os.path.exists("data.txt"):
    print("File exists")
else:
    print("File not found")
```

---

# 7. Deleting a File

```python
import os

os.remove("data.txt")
```

---

# 8. Example Program

```python
# Writing data to file
with open("students.txt", "w") as f:
    f.write("Varun\n")
    f.write("Rahul\n")

# Reading data from file
with open("students.txt", "r") as f:
    print(f.read())
```

---

# 9. Important File Methods

| Method       | Description          |
| ------------ | -------------------- |
| read()       | Reads entire file    |
| readline()   | Reads one line       |
| readlines()  | Reads all lines      |
| write()      | Writes data          |
| writelines() | Writes list of lines |
| close()      | Closes the file      |

---

# 10. File Pointer Functions

## tell()

Returns the **current position of the file pointer**.

```python
file.tell()
```

## seek()

Moves the file pointer to a specified location.

```python
file.seek(position)
```

### Example

```python
with open("data.txt","r") as f:
    print(f.tell())
    f.read(5)
    print(f.tell())
```

---

# Real World Use Cases

* Saving logs
* Storing configuration files
* Reading datasets for data science
* Writing reports
* Data preprocessing

---
