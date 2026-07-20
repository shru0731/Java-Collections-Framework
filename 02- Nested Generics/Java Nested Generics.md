# Java Nested Generics (Complete Notes) 🚀

Nested Generics means using **one generic type inside another generic type**.

---

# General Syntax

```java
Outer<Inner<Type>>
```

Example

```java
List<List<Integer>>
```

Read it **from inside to outside**.

```text
Integer
   ↓
List<Integer>
   ↓
List<List<Integer>>
```

Meaning:

> A `List` that stores `List<Integer>` objects.

---

# Why Nested Generics?

Suppose you want to store a matrix like this:

```text
[
 [1,2,3],
 [4,5,6],
 [7,8,9]
]
```

A normal list cannot store this structure.

```java
List<Integer> numbers = new ArrayList<>();
```

This stores

```text
[1,2,3,4,5]
```

To store rows, use a nested list:

```java
List<List<Integer>> matrix = new ArrayList<>();
```

Each element of `matrix` is another `List<Integer>`.

---

# Generic Syntax Pattern

## Single Generic

```java
List<Integer> numbers;
```

Represents

```text
List
 ├── 10
 ├── 20
 ├── 30
```

---

## Nested Generic

```java
List<List<Integer>> matrix;
```

Represents

```text
List
 ├── List<Integer>
 ├── List<Integer>
 ├── List<Integer>
```

---

# Declaration Types

## Type 1 (Recommended)

```java
List<List<Integer>> list = new ArrayList<>();
```

- Uses interface as reference
- Flexible
- Best practice

---

## Type 2

```java
ArrayList<ArrayList<Integer>> list =
        new ArrayList<>();
```

- Uses concrete implementation
- Less flexible

---

## Type 3

```java
List<LinkedList<Integer>> list =
        new ArrayList<>();
```

Outer Collection

- List

Inner Collection

- LinkedList

---

## Type 4

```java
List<Vector<Integer>> list =
        new ArrayList<>();
```

---

## Type 5

```java
List<Stack<Integer>> list =
        new ArrayList<>();
```

---

# Creating a Nested List

```java
List<List<Integer>> matrix = new ArrayList<>();
```

Initially

```text
[]
```

Create rows

```java
List<Integer> row1 = new ArrayList<>();
List<Integer> row2 = new ArrayList<>();
```

Add values

```java
row1.add(1);
row1.add(2);
row1.add(3);

row2.add(4);
row2.add(5);
row2.add(6);
```

Add rows

```java
matrix.add(row1);
matrix.add(row2);
```

Output

```text
[
 [1,2,3],
 [4,5,6]
]
```

---

# Common Methods

## add()

Adds a new row.

```java
matrix.add(row);
```

Example

```java
matrix.add(Arrays.asList(10,20,30));
```

Output

```text
[
 [10,20,30]
]
```

---

## get()

Returns a row.

```java
matrix.get(index);
```

Example

```java
matrix.get(0);
```

Output

```text
[10,20,30]
```

Return Type

```java
List<Integer>
```

---

## Nested get()

```java
matrix.get(0).get(2);
```

Explanation

```text
matrix

↓

[
 [10,20,30],
 [40,50,60]
]

↓

matrix.get(0)

↓

[10,20,30]

↓

matrix.get(0).get(2)

↓

30
```

Return Type

```java
Integer
```

---

## set()

Replace an entire row

```java
matrix.set(0, new ArrayList<>());
```

Replace a single element

```java
matrix.get(0).set(1,100);
```

Before

```text
[10,20,30]
```

After

```text
[10,100,30]
```

---

## remove()

Remove a row

```java
matrix.remove(0);
```

Remove an element from a row

```java
matrix.get(1).remove(2);
```

---

## size()

Outer size

```java
matrix.size();
```

Returns

```text
Number of rows
```

Example

```text
3
```

Inner size

```java
matrix.get(0).size();
```

Returns

```text
Number of columns
```

Example

```text
5
```

---

## clear()

```java
matrix.clear();
```

Removes all rows.

---

## contains()

```java
matrix.contains(row1);
```

Checks whether a row exists.

---

# Traversing a Nested List

## Method 1 - Normal for Loop

```java
for(int i = 0; i < matrix.size(); i++)
{
    for(int j = 0; j < matrix.get(i).size(); j++)
    {
        System.out.print(matrix.get(i).get(j) + " ");
    }
    System.out.println();
}
```

Output

```text
1 2 3
4 5 6
```

---

## Method 2 - Enhanced for Loop

```java
for(List<Integer> row : matrix)
{
    for(Integer num : row)
    {
        System.out.print(num + " ");
    }
    System.out.println();
}
```

---

# Adding Rows Directly

```java
matrix.add(Arrays.asList(1,2,3));

matrix.add(Arrays.asList(4,5,6));
```

Output

```text
[
 [1,2,3],
 [4,5,6]
]
```

---

# Common Nested Generic Types

## List of Lists

```java
List<List<Integer>>
```

Stores

```text
[
 [1,2],
 [3,4]
]
```

---

## List of Set

```java
List<Set<Integer>>
```

Stores

```text
[
 {1,2},
 {4,5}
]
```

---

## List of Queue

```java
List<Queue<Integer>>
```

---

## List of Stack

```java
List<Stack<Integer>>
```

---

## List of Map

```java
List<Map<Integer,String>>
```

Example

```text
[
 {1=A,2=B},
 {3=C,4=D}
]
```

---

## Set of List

```java
Set<List<Integer>>
```

---

## Queue of List

```java
Queue<List<Integer>>
```

---

## Map with List

```java
Map<Integer,List<String>>
```

Example

```text
1
↓
["Java","Python"]

2
↓
["C","C++"]
```

---

## Map with Set

```java
Map<String,Set<Integer>>
```

---

## Map with Queue

```java
Map<Integer,Queue<String>>
```

---

## Map of Map

```java
Map<Integer,Map<String,Integer>>
```

Example

```text
1
↓

{
 Math=90,
 Java=95
}
```

---

# Multi-Level Nested Generics

```java
List<List<List<Integer>>>
```

Represents a **3D List**.

Example

```text
[
   [
      [1,2],
      [3,4]
   ],

   [
      [5,6],
      [7,8]
   ]
]
```

---

# Common Interview Examples

## Matrix

```java
List<List<Integer>> matrix =
        new ArrayList<>();
```

---

## Graph (Adjacency List)

```java
List<List<Integer>> graph =
        new ArrayList<>();
```

Graph

```text
0 → 1 2

1 → 2

2 → 3

3 → 0
```

Stored as

```text
[
 [1,2],
 [2],
 [3],
 [0]
]
```

---

## Group Anagrams

```java
List<List<String>>
```

Output

```text
[
 ["eat","tea","ate"],
 ["bat"],
 ["tan","nat"]
]
```

---

# Memory Trick

Always read nested generics **from the inside out**.

Example

```java
List<List<Integer>>
```

Read as

```text
Integer

↓

List<Integer>

↓

List<List<Integer>>
```

Meaning

> A `List` containing `List<Integer>` objects.

---

Another Example

```java
Map<String,List<Integer>>
```

Read as

```text
Integer

↓

List<Integer>

↓

Map<String,List<Integer>>
```

Meaning

> A `Map` where each `String` key maps to a `List<Integer>`.

---

# Quick Reference Table

| Declaration | Meaning |
|-------------|---------|
| `List<Integer>` | List of Integers |
| `List<String>` | List of Strings |
| `List<List<Integer>>` | List of Integer Lists (2D List) |
| `Set<List<Integer>>` | Set containing Lists |
| `List<Set<Integer>>` | List containing Sets |
| `Queue<List<Integer>>` | Queue containing Lists |
| `Map<Integer,String>` | Integer → String mapping |
| `Map<Integer,List<String>>` | Integer → List of Strings |
| `Map<String,Set<Integer>>` | String → Set of Integers |
| `Map<Integer,Map<String,Integer>>` | Integer → Map of String to Integer |
| `List<Map<Integer,String>>` | List containing Maps |
| `List<List<List<Integer>>>` | 3D List |

---

# Interview Tips 💡

- Always read nested generics **from the innermost type outward**.
- Prefer **interfaces** (`List`, `Set`, `Map`, `Queue`) on the left-hand side and concrete implementations (`ArrayList`, `HashSet`, `HashMap`, etc.) on the right-hand side.
- `List<List<Integer>>` is commonly used to represent:
  - Matrices
  - Graph adjacency lists
  - Grouped data (e.g., Group Anagrams)
- `Map<K, List<V>>` is useful when one key maps to multiple values.
- `Map<K, Set<V>>` ensures the values associated with each key are unique.
- Deeply nested generics (three or more levels) are powerful but can reduce readability. Use them only when they model the data naturally.