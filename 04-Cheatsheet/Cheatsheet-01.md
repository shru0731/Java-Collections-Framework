# How to Remember Java Collection Methods (Study Notes) 🧠

One of the biggest mistakes beginners make is trying to **memorize every method** in the Java Collections Framework.

**Don't memorize methods. Learn them by category and usage.**

Experienced Java developers also don't remember every method—they remember **patterns**.

---

# Step 1: Learn the Core Collection Methods First ⭐

These methods are common to almost every Collection (`List`, `Set`, `Queue`).

| Method | Purpose |
|---------|---------|
| `add()` | Insert an element |
| `remove()` | Delete an element |
| `contains()` | Check whether an element exists |
| `size()` | Returns the number of elements |
| `isEmpty()` | Checks whether the collection is empty |
| `clear()` | Removes all elements |
| `iterator()` | Used for traversal |
| `toArray()` | Converts collection to an array |

> **Memory Trick:**  
> **Add → Remove → Search → Count → Empty → Clear → Traverse → Convert**

---

# Step 2: Remember Methods by Data Structure

Instead of remembering 100 methods, remember what each data structure is designed to do.

---

# 📋 List

## Think: **Index-Based Collection**

A List stores elements in order and allows duplicates.

Since it has indexes, ask yourself:

> **"What operations can I perform using an index?"**

### Important Methods

```java
add();

get();

set();

remove();

indexOf();

lastIndexOf();

contains();

size();

clear();
```

### Memory Trick

```text
ADD
GET
SET
REMOVE
INDEX
```

Remember:

> **List = Add → Get → Set → Remove → Index**

---

# 🌳 Set

## Think: **Unique Elements**

A Set does **not** have indexes.

So there is no:

```java
get()
```

Important methods

```java
add();

remove();

contains();

size();

clear();

isEmpty();
```

### Memory Trick

```text
UNIQUE

ADD

REMOVE

SEARCH
```

Remember:

> **Set = Store Unique Elements**

---

# 🚶 Queue

## Think: **People Standing in a Queue**

Imagine people waiting in line.

You can

```java
offer();   // Join the queue

peek();    // Look at first person

poll();    // Remove first person
```

### Memory Trick

```text
Offer

Peek

Poll
```

Remember:

> **Queue = Offer → Peek → Poll**

---

# 🗺️ Map

## Think: **Dictionary**

A Map stores

```text
Key → Value
```

Important methods

```java
put();

get();

remove();

containsKey();

containsValue();

keySet();

values();

entrySet();
```

### Memory Trick

```text
PUT

GET

KEY

VALUE
```

Remember:

> **Map = Put → Get → Remove → Keys → Values**

---

# 📦 Arrays Utility Class

Works only with arrays.

Most frequently used methods

```java
Arrays.sort(arr);

Arrays.binarySearch(arr,key);

Arrays.fill(arr,value);

Arrays.copyOf(arr,newLength);

Arrays.equals(arr1,arr2);

Arrays.toString(arr);

Arrays.deepToString(matrix);
```

### Memory Trick

```text
SORT

SEARCH

COPY

PRINT
```

---

# 📚 Collections Utility Class

Works with Collection Framework classes like List.

Most frequently used methods

```java
Collections.sort(list);

Collections.reverse(list);

Collections.shuffle(list);

Collections.swap(list,i,j);

Collections.max(list);

Collections.min(list);

Collections.frequency(list,value);

Collections.binarySearch(list,key);
```

### Memory Trick

```text
SORT

REVERSE

SHUFFLE

MAX

MIN
```

---

# ➗ Math Class

Most frequently used methods

```java
Math.max();

Math.min();

Math.abs();

Math.pow();

Math.sqrt();

Math.random();

Math.ceil();

Math.floor();

Math.round();
```

### Memory Trick

```text
MAX

MIN

POWER

ROOT

RANDOM

ROUND
```

---

# 🔤 String Methods

Most commonly used methods

```java
length();

charAt();

substring();

contains();

equals();

replace();

split();

trim();

toUpperCase();

toLowerCase();
```

### Memory Trick

```text
LENGTH

CHARACTER

SUBSTRING

REPLACE

SPLIT
```

---

# Step 3: Learn by Real-Life Analogy

## List

Think of a notebook.

You can

```java
add()

get()

set()

remove()
```

because every page has a number (index).

---

## Set

Think of an attendance register.

Duplicate names are not allowed.

You can

```java
add()

remove()

contains()
```

---

## Queue

Think of people standing in a bank queue.

```text
Offer → Join

Peek → See first person

Poll → Remove first person
```

---

## Map

Think of a dictionary.

```text
Word → Meaning

Student ID → Name

Employee ID → Salary
```

Everything is stored as

```text
Key → Value
```

---

# Step 4: Practice Instead of Memorizing

Writing code repeatedly is the fastest way to remember methods.

Example

```java
ArrayList<Integer> list = new ArrayList<>();

list.add(10);

list.add(20);

list.remove(0);

list.set(0,100);

System.out.println(list.get(0));

System.out.println(list.contains(100));

System.out.println(list.size());
```

Practice writing similar code daily.

---

# Step 5: Learn Only the Most Important Methods First

## Collection

```java
add()

remove()

contains()

size()

isEmpty()

clear()

iterator()
```

---

## List

```java
get()

set()

add()

remove()

indexOf()

lastIndexOf()
```

---

## Set

```java
add()

remove()

contains()
```

---

## Queue

```java
offer()

peek()

poll()
```

---

## Map

```java
put()

get()

remove()

containsKey()

keySet()

values()

entrySet()
```

---

## Arrays

```java
sort()

binarySearch()

fill()

copyOf()

equals()

toString()
```

---

## Collections

```java
sort()

reverse()

shuffle()

swap()

max()

min()

frequency()
```

---

# Quick Revision Cheat Sheet

| Data Structure / Class | Remember These Methods |
|------------------------|------------------------|
| **Collection** | `add()`, `remove()`, `contains()`, `size()`, `isEmpty()`, `clear()` |
| **List** | `get()`, `set()`, `add()`, `remove()`, `indexOf()` |
| **Set** | `add()`, `remove()`, `contains()` |
| **Queue** | `offer()`, `peek()`, `poll()` |
| **Map** | `put()`, `get()`, `remove()`, `containsKey()`, `keySet()`, `values()`, `entrySet()` |
| **Arrays** | `sort()`, `binarySearch()`, `fill()`, `copyOf()`, `equals()`, `toString()` |
| **Collections** | `sort()`, `reverse()`, `shuffle()`, `swap()`, `max()`, `min()`, `frequency()` |
| **Math** | `max()`, `min()`, `pow()`, `sqrt()`, `abs()`, `random()` |
| **String** | `length()`, `charAt()`, `substring()`, `contains()`, `replace()`, `split()` |
