# 🐍 Python Practice — Day 5: Tuples & Sets
 
A project-based walkthrough of two core Python data structures — **Tuples** and **Sets** — ending with a mini course-enrollment analyzer built entirely with set operations.
 
---
 
## 📌 Topics Covered
- Tuple creation & indexing
- Tuple unpacking
- Set creation & uniqueness
- Adding & removing elements from a set
- Membership checks (`in`)
- Set operations: `intersection()`, `union()`, `difference()`
- Combining dictionaries + sets
- Final challenge: a course enrollment analyzer
---
 
## 🔹 Tuples
 
### Exercise 1 — Creating a Tuple
```python
info = ("Jaymin", 21, "Ai/Ml")
print("Your Name =", info[0])
print("Your Age =", info[1])
print("Your Course =", info[2])
```
 
### Exercise 2 — Tuple Unpacking
```python
name, age, course = ("Jaymin", 21, "Ai/Ml")
print("Your Name =", name)
print("Your Age =", age)
print("Your Course =", course)
```
 
---
 
## 🔹 Sets
 
A set automatically keeps only **unique values**.
 
```python
subjects = {"Python", "Math", "Python", "Physics", "Math"}
print(subjects)
# duplicates are dropped automatically
```
 
### Exercise 1 — Add a Value
```python
subjects = {"Python", "Math", "Physics"}
subjects.add("Ai")
print(subjects)
```
 
### Exercise 2 — Remove a Value
```python
subjects = {"Python", "Math", "Physics", "Ai"}
subjects.remove("Math")
print(subjects)
```
 
### Exercise 3 — Membership Check (`in`)
```python
subjects = {"Python", "Math", "Physics", "Ai"}
if "Python" in subjects:
    print("Python is present")
else:
    print("Python is not present")
```
 
### Exercise 4 — Set Operations
 
**Intersection** — common elements between two sets:
```python
python_students = {"Jaymin", "Rahul", "Aman", "Priya"}
ml_students = {"Jaymin", "Aman", "Riya", "Karan"}
same_student = python_students.intersection(ml_students)
print(same_student)
```
 
**Union** — all unique elements from both sets:
```python
all_student = python_students.union(ml_students)
print(all_student)
```
 
**Difference** — elements in one set but not the other:
```python
python_only = python_students.difference(ml_students)
print(python_only)
```
 
### Exercise 5 — Mini Challenge: Dictionary + Sets
```python
student = {
    "python_students": {"Jaymin", "Rahul", "Aman", "Priya"},
    "ml_students": {"Jaymin", "Aman", "Riya", "Karan"}
}
 
test = student["python_students"].intersection(student["ml_students"])
print(test)
```
 
---
 
## 🏆 Final Challenge — Course Enrollment Analyzer
 
**Goal:** Using only dictionary access + sets, find:
1. Students taking both Python and ML
2. Students taking Python but not ML
3. All unique students across all three courses
```python
courses = {
    "Python": {"Jaymin", "Rahul", "Aman", "Priya"},
    "ML": {"Jaymin", "Aman", "Riya"},
    "Web": {"Rahul", "Priya", "Karan"}
}
 
intersection_students = courses["Python"].intersection(courses["ML"])
print("Students taking both Python and ML are", intersection_students)
 
python_only = courses["Python"].difference(courses["ML"])
print("Students taking Python but not ML are", python_only)
 
unique_students = courses["Python"].union(courses["ML"], courses["Web"])
print("All unique students across all three courses are", unique_students)
```
 
**Output:**
```
Students taking both Python and ML are {'Jaymin', 'Aman'}
Students taking Python but not ML are {'Rahul', 'Priya'}
All unique students across all three courses are {'Jaymin', 'Rahul', 'Aman', 'Priya', 'Riya', 'Karan'}
```
 
---
 
## 🧠 Key Takeaways
- **Tuples** are ordered, immutable — great for fixed data like `(name, age, course)`.
- **Sets** are unordered, mutable, and automatically remove duplicates.
- Set operations (`intersection`, `union`, `difference`) make comparing groups of data fast and readable — no manual loops needed.
- Combining dictionaries with sets is a powerful pattern for organizing and querying grouped data (e.g., course rosters).
---
 
*Day 5 of my Python learning journey — building a strong foundation one data structure at a time.* 🚀
 
`#Python #100DaysOfCode #AIML #LearningInPublic`
