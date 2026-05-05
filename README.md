# 📚 Student Performance Management System

## 🧾 Overview

The **Student Performance Management System** is a console-based Java application designed to manage and analyze student academic data using the **Java Collection Framework**.

This project demonstrates real-world usage of collections, object-oriented design, and efficient data handling techniques in Java.

---

## 🎯 Objectives

* Implement core concepts of the **Java Collection Framework**
* Demonstrate usage of:

    * List, Set, Map, Queue
    * Generics and type safety
    * Iterators and safe modification
    * Sorting using Comparable and Comparator
* Build a modular, scalable console-based application

---

## 🚀 Features

### 👨‍🎓 Student Management

* Add new students with unique ID
* Prevent duplicate student entries
* Delete students safely using Iterator

### 📊 Marks Management

* Add and update subject-wise marks
* Prevent duplicate subjects
* Validate marks (0–100 range)

### 🔍 Search & View

* Search student by ID (**O(1)** using HashMap)
* View student details:

    * Name, ID
    * Subject-wise marks
    * Average score
    * Grade

### 📈 Sorting

* Sort students by:

    * ID (default – Comparable)
    * Name (Comparator)
    * Average marks (Comparator)

### 🏆 Top Performers

* Display top N students
* Uses PriorityQueue (Heap-based ranking)

---

## 🧠 Collections Used

| Collection    | Usage           | Reason             |
| ------------- | --------------- | ------------------ |
| HashMap       | Store students  | Fast lookup (O(1)) |
| ArrayList     | Sorting         | Easy iteration     |
| HashSet       | Unique subjects | Prevent duplicates |
| PriorityQueue | Top performers  | Efficient ranking  |

---

## ⚙️ Internal Working Concepts

### 🔹 HashMap

* Uses `hashCode()` to calculate bucket index
* Handles collisions using chaining (LinkedList / Tree)
* Provides O(1) average time complexity

### 🔹 Iterator (Fail-Fast)

* Used for safe removal during iteration
* Prevents `ConcurrentModificationException`

### 🔹 PriorityQueue (Heap)

* Maintains elements in sorted order (based on comparator)
* Efficient extraction of top elements

### 🔹 Comparable vs Comparator

* Comparable → Default sorting (by ID)
* Comparator → Custom sorting (Name, Average)

---

## 🧱 Project Structure

```
com.project
├── model
│   └── Student.java
├── service
│   └── StudentService.java
├── util
│   └── SortUtil.java
├── exception
│   └── DuplicateStudentException.java
├── main
│   └── Main.java
```

---

## 🛠️ Technologies Used

* Java (Core Java)
* Java Collection Framework
* OOP Principles

---

## ▶️ How to Run

### Compile

```bash
javac com/project/**/*.java
```

### Run

```bash
java com.project.main.Main
```

---

## 📌 Sample Menu

```
1. Add Student
2. Add/Update Marks
3. View Student
4. Delete Student
5. Search Student
6. Sort Students
7. Top Performers
8. Exit
```

---

## ⚠️ Exception Handling

* Duplicate student ID → Custom Exception
* Invalid marks → IllegalArgumentException
* Invalid input → Handled via try-catch

---

## 🧪 Test Scenarios

* Add duplicate student
* Add duplicate subject
* Delete student during iteration
* Sort students by different criteria
* Handle empty dataset

---

## 📊 Complexity Overview

| Operation      | Complexity |
| -------------- | ---------- |
| Add Student    | O(1)       |
| Search Student | O(1)       |
| Add Marks      | O(1)       |
| Sorting        | O(n log n) |
| Top Performers | O(n log n) |

---

## 💡 Key Design Decisions

* Used **HashMap** for fast lookup
* Used **HashSet** to enforce unique subjects
* Used **PriorityQueue** for efficient ranking
* Encapsulated validation inside model class
* Maintained modular architecture

---

## 📌 Learning Outcomes

* Deep understanding of Java Collections
* Practical implementation of OOP principles
* Handling real-world edge cases
* Writing clean, maintainable code

---

## 🏁 Conclusion

This project serves as a strong foundation for understanding:

* Data structures in Java
* Real-world application design
* Efficient data processing using collections

---

✨ *This project is ideal for interview preparation and strengthening core Java concepts.*
