# Section 5. Lists & Tuples

## Topics
- List – creation and manipulation.
- Tuple – immutable sequences.
- List methods - `append(x)` • `extend(iterable)` • `insert(i, x)` • `remove(x)` • `pop([i])` • `clear()` • `index(x[, start[, end]])` • `count(x)` • `sort(key=None, reverse=False)` • `reverse()` • `copy()` • `len(lst)` • `sum(lst)` • `min(lst)` • `max(lst)` • `sum(lst)/len(lst)` (average)
- Nested lists (2D lists)
- Sort a list in place
- Sort a list (with `sorted()`)
- Slice a list
- Unpack a list
- Iterate over a list
- Find the index of an element
- Iterables and Iterators
- Transform list elements with `map()`
- Filter list elements with `filter()`
- Reduce list elements into a value with `reduce()`
- List comprehensions


# Python Practical Questions – Lists, Tuples & List Methods

---

## 1. Create a List
Write a program that:
- Creates a list of 5 city names  
- Prints the complete list  
- Prints the third city name  

---

## 2. Create a Tuple
Write a program that:
- Creates a tuple of 4 subject names  
- Prints all values  
- Prints type of tuple using `type()`  

---

## 3. Mutable vs Immutable
Write a program that:
- Creates a list and changes one value  
- Creates a tuple and tries to change one value  
- Observe and explain the output  

---

## 4. append() Method
Write a program that:
- Creates a list of numbers `[5,10,15,20]`  
- Adds `25` using `append()`  
- Prints updated list  

---

## 5. insert() Method
Write a program that:
- Creates a list `[100,200,300,400]`  
- Inserts `150` at index `1`  
- Prints updated list  

---

## 6. remove() and pop() Methods
Write a program that:
- Creates a list `[11,22,33,44,55]`  
- Removes `33` using `remove()`  
- Removes last element using `pop()`  
- Prints updated list  

---

## 7. sort() and reverse()
Write a program that:
- Creates a list `[45,12,78,34,23]`  
- Sorts the list  
- Reverses the sorted list  
- Prints both outputs  

---

## 8. extend() Method
Write a program that:
- Creates two lists:
  - `[1,2,3]`
  - `[4,5,6]`
- Combines both using `extend()`  
- Prints final list  

---

## 9. clear() Method
Write a program that:
- Creates a list of 5 values  
- Clears all elements using `clear()`  
- Prints final list  

---

## 10. Nested Lists (2D Lists)
Write a program that:
- Creates a nested list:
```python
marks = [
    [80, 85, 90],
    [70, 75, 78],
    [88, 92, 95]
]
