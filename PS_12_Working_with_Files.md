# Section 12. Working with Files

## Topics
- Read from a text file
- Write to a text file
- Create a new text file
- Check if a file exists
- Read CSV files (`csv` module)
- Write CSV files (`csv` module)
- Rename a file
- Delete a file
- Read & Write JSON files (`json` module)
- File path management with `os.path` & `pathlib`
---

# 1. Read from a Text File

Use `open()` with **read mode (`r`)** to read a file.

```python
with open("data.txt", "r") as file:
    content = file.read()
    print(content)
```

Read line by line:

```python
with open("data.txt", "r") as file:
    for line in file:
        print(line)
```

---

# 2. Write to a Text File

Use **write mode (`w`)** to write data to a file.

⚠ This **overwrites existing content**.

```python
with open("data.txt", "w") as file:
    file.write("Hello Python\n")
    file.write("File handling example")
```

---

# 3. Create a New Text File

Use **`x` mode** to create a new file.

```python
with open("newfile.txt", "x") as file:
    file.write("This is a new file")
```

If the file already exists, Python will raise an error.

---

# 4. Check if a File Exists

Use the **os module**.

```python
import os

if os.path.exists("data.txt"):
    print("File exists")
else:
    print("File does not exist")
```

---

# 5. Read CSV Files (csv module)

The **csv module** is used to read comma-separated values files.

```python
import csv

with open("data.csv", "r") as file:
    reader = csv.reader(file)

    for row in reader:
        print(row)
```

Each row is returned as a **list**.

Example CSV file:

```
Name,Age,City
Varun,25,Delhi
Rahul,22,Mumbai
```

---

# 6. Write CSV Files (csv module)

```python
import csv

data = [
    ["Name", "Age", "City"],
    ["Varun", 25, "Delhi"],
    ["Rahul", 22, "Mumbai"]
]

with open("data.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

---

# 7. Rename a File

Use **os.rename()**.

```python
import os

os.rename("oldname.txt", "newname.txt")
```

---

# 8. Delete a File

Use **os.remove()**.

```python
import os

os.remove("data.txt")
```

---

# 9. Read & Write JSON Files (json module)

JSON is commonly used for **data exchange in APIs and applications**.

## Write JSON

```python
import json

data = {
    "name": "Varun",
    "age": 25,
    "city": "Delhi"
}

with open("data.json", "w") as file:
    json.dump(data, file)
```

---

## Read JSON

```python
import json

with open("data.json", "r") as file:
    data = json.load(file)

print(data)
```

---

# 10. File Path Management (os.path & pathlib)

## Using os.path

```python
import os

print(os.path.exists("data.txt"))
print(os.path.abspath("data.txt"))
print(os.path.basename("folder/data.txt"))
```

---

## Using pathlib (Modern Approach)

```python
from pathlib import Path

path = Path("data.txt")

print(path.exists())
print(path.name)
print(path.absolute())
```

---

# Summary of Important Modules

| Module  | Purpose                       |
| ------- | ----------------------------- |
| os      | File and system operations    |
| os.path | File path utilities           |
| csv     | Reading and writing CSV files |
| json    | Working with JSON data        |
| pathlib | Modern file path management   |

---

# Real World Use Cases

* Reading datasets for **data analysis**
* Exporting reports to **CSV**
* Storing configuration in **JSON**
* Managing files in automation scripts
* Building **data pipelines**

---
