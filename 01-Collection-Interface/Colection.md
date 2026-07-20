# Java Collections Framework 🚀

A complete quick-reference guide to the Java Collections Framework.

---

# Package

```java
import java.util.*;
```

---

# Collection Hierarchy

```text
Iterable
    |
Collection
    |
-------------------------------------------------
|              |               |
List          Set            Queue
 |             |                |
ArrayList    HashSet      PriorityQueue
LinkedList   LinkedHashSet
Vector       TreeSet
Stack
```

```text
Map (Not part of Collection Interface)

             Map
              |
-----------------------------------------
|              |              |
HashMap    LinkedHashMap    TreeMap
```

---

# 1. Collection Interface

The **Collection** interface is the parent interface of **List**, **Set**, and **Queue**.

## Declaration

```java
Collection<DataType> obj = new ArrayList<>();
```

Example

```java
Collection<Integer> numbers = new ArrayList<>();
```

---

## Common Methods

| Method | Description |
|---------|-------------|
| `add(element)` | Adds an element |
| `remove(element)` | Removes an element |
| `size()` | Returns number of elements |
| `isEmpty()` | Checks whether the collection is empty |
| `clear()` | Removes all elements |
| `contains(element)` | Checks if an element exists |
| `iterator()` | Returns an Iterator |
| `toArray()` | Converts collection to an array |

---

## Example

```java
Collection<String> fruits = new ArrayList<>();

fruits.add("Apple");
fruits.add("Banana");

System.out.println(fruits);

fruits.remove("Apple");

System.out.println(fruits.size());

System.out.println(fruits.contains("Banana"));

fruits.clear();
```

---

# 2. List Interface

A **List** stores ordered elements.

## Features

- Ordered
- Duplicates allowed
- Index-based access

---

## Declaration

```java
List<DataType> list = new ArrayList<>();
```

or

```java
List<DataType> list = new LinkedList<>();
```

or

```java
List<DataType> list = new Vector<>();
```

Example

```java
List<String> names = new ArrayList<>();
```

---

## Common List Methods

### Add

```java
list.add(value);
list.add(index, value);
```

Example

```java
list.add("A");
list.add("B");
list.add(1, "C");
```

---

### Get

```java
list.get(index);
```

Example

```java
System.out.println(list.get(0));
```

---

### Set

Replaces an element.

```java
list.set(index, value);
```

Example

```java
list.set(1, "Java");
```

---

### Remove

```java
list.remove(index);
list.remove(object);
```

Example

```java
list.remove(2);
list.remove("Java");
```

---

### Other Methods

```java
list.size();

list.contains(value);

list.indexOf(value);

list.lastIndexOf(value);

list.clear();
```

---

### Sorting

Ascending

```java
Collections.sort(list);
```

Descending

```java
Collections.sort(list, Collections.reverseOrder());
```

---

### Reverse

```java
Collections.reverse(list);
```

---

### Shuffle

```java
Collections.shuffle(list);
```

---

# ArrayList

## Declaration

```java
ArrayList<Integer> list = new ArrayList<>();
```

With Initial Capacity

```java
ArrayList<Integer> list = new ArrayList<>(20);
```

Copy Another List

```java
ArrayList<Integer> copy = new ArrayList<>(list);
```

---

# LinkedList

## Declaration

```java
LinkedList<String> list = new LinkedList<>();
```

### Additional Methods

```java
list.addFirst(value);

list.addLast(value);

list.removeFirst();

list.removeLast();

list.getFirst();

list.getLast();
```

---

# Vector

## Declaration

```java
Vector<Integer> vector = new Vector<>();
```

With Capacity

```java
Vector<Integer> vector = new Vector<>(10);
```

---

# Stack

## Declaration

```java
Stack<Integer> stack = new Stack<>();
```

### Methods

Push

```java
stack.push(10);
```

Pop

```java
stack.pop();
```

Peek

```java
stack.peek();
```

Search

```java
stack.search(value);
```

Empty

```java
stack.empty();
```

---

# 3. Set Interface

A **Set** stores unique elements.

## Features

- No duplicates
- Unordered (except LinkedHashSet and TreeSet)

---

## Declaration

```java
Set<Integer> set = new HashSet<>();
```

or

```java
Set<Integer> set = new LinkedHashSet<>();
```

or

```java
Set<Integer> set = new TreeSet<>();
```

---

# HashSet

```java
HashSet<String> set = new HashSet<>();
```

## Methods

```java
set.add(value);

set.remove(value);

set.contains(value);

set.size();

set.clear();

set.isEmpty();
```

---

# LinkedHashSet

```java
LinkedHashSet<Integer> set = new LinkedHashSet<>();
```

Maintains insertion order.

---

# TreeSet

```java
TreeSet<Integer> set = new TreeSet<>();
```

### Additional Methods

```java
set.first();

set.last();

set.higher(value);

set.lower(value);

set.ceiling(value);

set.floor(value);

set.pollFirst();

set.pollLast();
```

---

# 4. Queue Interface

A **Queue** follows the FIFO (First In, First Out) principle.

---

## Declaration

```java
Queue<Integer> queue = new LinkedList<>();
```

or

```java
Queue<Integer> queue = new PriorityQueue<>();
```

---

## Common Methods

Insert

```java
queue.offer(value);

queue.add(value);
```

Remove

```java
queue.poll();

queue.remove();
```

Peek

```java
queue.peek();

queue.element();
```

---

# PriorityQueue

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
```

Descending Order

```java
PriorityQueue<Integer> pq =
        new PriorityQueue<>(Collections.reverseOrder());
```

---

# Deque

```java
Deque<Integer> dq = new ArrayDeque<>();
```

### Methods

```java
dq.addFirst(value);

dq.addLast(value);

dq.offerFirst(value);

dq.offerLast(value);

dq.removeFirst();

dq.removeLast();

dq.pollFirst();

dq.pollLast();

dq.peekFirst();

dq.peekLast();
```

---

# 5. Map Interface

A **Map** stores key-value pairs.

- Keys are unique.
- Values can be duplicated.

---

## Declaration

```java
Map<KeyType, ValueType> map = new HashMap<>();
```

Example

```java
Map<Integer, String> map = new HashMap<>();
```

---

## Common Methods

Put

```java
map.put(key, value);
```

Get

```java
map.get(key);
```

Remove

```java
map.remove(key);
```

Contains

```java
map.containsKey(key);

map.containsValue(value);
```

Replace

```java
map.replace(key, value);
```

Other Methods

```java
map.size();

map.clear();

map.keySet();

map.values();

map.entrySet();
```

---

# HashMap

```java
HashMap<Integer, String> map = new HashMap<>();
```

---

# LinkedHashMap

```java
LinkedHashMap<Integer, String> map =
        new LinkedHashMap<>();
```

Maintains insertion order.

---

# TreeMap

```java
TreeMap<Integer, String> map = new TreeMap<>();
```

### Additional Methods

```java
map.firstKey();

map.lastKey();

map.higherKey(key);

map.lowerKey(key);

map.ceilingKey(key);

map.floorKey(key);

map.pollFirstEntry();

map.pollLastEntry();
```

---

# Traversing Collections

## Using Enhanced For Loop

```java
for (DataType element : collection)
{
    System.out.println(element);
}
```

Example

```java
for (String name : list)
{
    System.out.println(name);
}
```

---

## Using Iterator

```java
Iterator<DataType> itr = collection.iterator();

while (itr.hasNext())
{
    System.out.println(itr.next());
}
```

---

## Using ListIterator

```java
ListIterator<DataType> itr = list.listIterator();

while (itr.hasNext())
{
    System.out.println(itr.next());
}

while (itr.hasPrevious())
{
    System.out.println(itr.previous());
}
```

---

# Traversing a Map

## Using entrySet() (Recommended)

```java
for (Map.Entry<Integer, String> entry : map.entrySet())
{
    System.out.println(entry.getKey() + " " + entry.getValue());
}
```

---

## Using keySet()

```java
for (Integer key : map.keySet())
{
    System.out.println(key + " " + map.get(key));
}
```

---

# Collections Utility Class

```java
Collections.sort(list);

Collections.reverse(list);

Collections.shuffle(list);

Collections.max(list);

Collections.min(list);

Collections.swap(list, i, j);

Collections.frequency(list, value);

Collections.binarySearch(list, value);
```

---

# Comparator (Custom Sorting)

## Ascending (Default)

```java
Collections.sort(list);
```

---

## Descending

```java
Collections.sort(list, Collections.reverseOrder());
```

---

## Custom Comparator

```java
Collections.sort(list, new Comparator<String>() {
    @Override
    public int compare(String s1, String s2) {
        return Integer.compare(s1.length(), s2.length());
    }
});
```

---

## Lambda Expression (Java 8+)

```java
list.sort((s1, s2) -> Integer.compare(s1.length(), s2.length()));
```