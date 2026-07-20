# Java Utility Classes (Complete Notes) 🚀

## What is a Utility Class?

A **Utility Class** is a class that contains **only static methods** used to perform common operations. Since the methods are **static**, you do **not** create an object of the class. Instead, you call the methods using the **class name**.

---

# General Syntax

```java
ClassName.methodName(arguments);
```

Examples

```java
Arrays.sort(arr);

Collections.sort(list);

Math.sqrt(25);

Integer.parseInt("123");
```

---

# Why Static Methods?

Normally, to call a **non-static method**, you must create an object.

```java
class Student {

    void display() {
        System.out.println("Hello");
    }
}

Student s = new Student();
s.display();
```

---

Utility classes contain **static methods**, so no object is required.

```java
Arrays.sort(arr);
```

Example declaration

```java
public static void sort(int[] a)
```

---

# Common Utility Classes

| Utility Class | Package | Works On |
|---------------|---------|----------|
| `Arrays` | `java.util` | Arrays |
| `Collections` | `java.util` | Collections (`List`, `Set`, `Queue`, etc.) |
| `Math` | `java.lang` | Mathematical operations |
| `Objects` | `java.util` | Object utilities |
| `Integer`, `Double`, `Character`, etc. | `java.lang` | Wrapper utilities |
| `String` | `java.lang` | String operations |

---

# 1. Arrays Class

## Package

```java
import java.util.Arrays;
```

---

## Purpose

The **Arrays** class provides utility methods for working with **arrays**.

General Syntax

```java
Arrays.methodName(arguments);
```

---

## sort()

Sorts an array in **ascending order**.

Syntax

```java
Arrays.sort(arr);
```

Example

```java
int[] arr = {5,2,9,1};

Arrays.sort(arr);

System.out.println(Arrays.toString(arr));
```

Output

```text
[1, 2, 5, 9]
```

---

## sort(fromIndex, toIndex)

Sorts only a portion of the array.

Syntax

```java
Arrays.sort(arr, 1, 4);
```

- `fromIndex` → Inclusive
- `toIndex` → Exclusive

Example

```java
int[] arr = {9,5,3,8,2};

Arrays.sort(arr,1,4);

System.out.println(Arrays.toString(arr));
```

Output

```text
[9, 3, 5, 8, 2]
```

---

## binarySearch()

Searches a **sorted array**.

Syntax

```java
Arrays.binarySearch(arr,key);
```

Example

```java
int[] arr = {1,3,5,7,9};

int index = Arrays.binarySearch(arr,7);

System.out.println(index);
```

Output

```text
3
```

**Note**

- The array **must be sorted**.
- If the element is not found, Java returns a **negative insertion point**, not always `-1`.

---

## fill()

Fills every element with the same value.

Syntax

```java
Arrays.fill(arr,10);
```

Example

Before

```text
[1,2,3]
```

After

```text
[10,10,10]
```

---

## copyOf()

Creates a copy of an array.

Syntax

```java
int[] copy = Arrays.copyOf(arr,5);
```

Example

```java
int[] arr = {1,2,3};

int[] copy = Arrays.copyOf(arr,5);

System.out.println(Arrays.toString(copy));
```

Output

```text
[1,2,3,0,0]
```

---

## equals()

Compares two arrays.

Syntax

```java
Arrays.equals(arr1,arr2);
```

Returns

```text
true
false
```

---

## toString()

Prints a **1D array**.

Syntax

```java
System.out.println(Arrays.toString(arr));
```

Output

```text
[1, 2, 3, 4]
```

---

## deepToString()

Prints **nested arrays**.

Example

```java
int[][] matrix = {
    {1,2},
    {3,4}
};

System.out.println(Arrays.deepToString(matrix));
```

Output

```text
[[1, 2], [3, 4]]
```

---

## Common Method Signatures

```java
public static void sort(int[] a)

public static int binarySearch(int[] a, int key)

public static void fill(int[] a, int value)

public static int[] copyOf(int[] a, int newLength)

public static boolean equals(int[] a, int[] b)

public static String toString(int[] a)
```

---

# 2. Collections Class

## Package

```java
import java.util.Collections;
```

---

## Purpose

The **Collections** class provides utility methods for working with Java Collection Framework classes such as:

- List
- ArrayList
- LinkedList
- Vector
- Stack
- Queue

General Syntax

```java
Collections.methodName(collection);
```

---

## sort()

Sorts a list in ascending order.

```java
Collections.sort(list);
```

---

## reverse()

Reverses the list.

```java
Collections.reverse(list);
```

---

## shuffle()

Randomly shuffles the list.

```java
Collections.shuffle(list);
```

---

## max()

Returns the largest element.

```java
Collections.max(list);
```

---

## min()

Returns the smallest element.

```java
Collections.min(list);
```

---

## frequency()

Counts occurrences of an element.

```java
Collections.frequency(list, value);
```

---

## binarySearch()

Searches a sorted list.

```java
Collections.binarySearch(list,key);
```

---

## swap()

Swaps two elements.

```java
Collections.swap(list,0,2);
```

---

## reverseOrder()

Sorts a list in descending order.

```java
Collections.sort(list, Collections.reverseOrder());
```

---

# Arrays vs Collections

| Arrays | Collections |
|---------|-------------|
| Works on arrays | Works on Collection objects |
| `Arrays.sort(arr)` | `Collections.sort(list)` |
| `Arrays.binarySearch()` | `Collections.binarySearch()` |
| `Arrays.fill()` | No equivalent |
| `Arrays.toString()` | `System.out.println(list)` |

---

# 3. Math Class

## Package

```java
java.lang
```

No import required.

---

## sqrt()

```java
Math.sqrt(25);
```

Returns

```text
5.0
```

---

## pow()

```java
Math.pow(2,5);
```

Returns

```text
32.0
```

---

## max()

```java
Math.max(10,20);
```

Returns

```text
20
```

---

## min()

```java
Math.min(10,20);
```

Returns

```text
10
```

---

## abs()

```java
Math.abs(-10);
```

Returns

```text
10
```

---

## random()

```java
Math.random();
```

Returns

```text
0.0 <= value < 1.0
```

Generate a random integer between **1 and 100**

```java
int num = (int)(Math.random() * 100) + 1;
```

---

## ceil()

```java
Math.ceil(5.2);
```

Returns

```text
6.0
```

---

## floor()

```java
Math.floor(5.9);
```

Returns

```text
5.0
```

---

## round()

```java
Math.round(5.7);
```

Returns

```text
6
```

---

# 4. Wrapper Classes

Wrapper classes convert between **primitive types** and **objects**.

---

## Integer

### parseInt()

```java
int n = Integer.parseInt("123");
```

---

### valueOf()

```java
Integer obj = Integer.valueOf("123");
```

---

### toString()

```java
String s = Integer.toString(100);
```

---

### compare()

```java
Integer.compare(10,20);
```

Returns

```text
-1
0
1
```

---

## Double

```java
Double.parseDouble("12.5");
```

---

## Character

```java
Character.isDigit(ch);

Character.isLetter(ch);

Character.isUpperCase(ch);

Character.isLowerCase(ch);

Character.toUpperCase(ch);

Character.toLowerCase(ch);
```

---

## Boolean

```java
Boolean.parseBoolean("true");
```

---

# 5. Objects Class

## Package

```java
import java.util.Objects;
```

---

## equals()

Null-safe comparison.

```java
Objects.equals(a,b);
```

---

## hash()

```java
Objects.hash(obj);
```

---

## requireNonNull()

```java
Objects.requireNonNull(name);
```

Throws a `NullPointerException` if the object is `null`.

---

# 6. String Utility Methods

Package

```java
java.lang
```

No import required.

Common Methods

```java
str.length();

str.charAt(index);

str.substring(start,end);

str.contains(text);

str.equals(other);

str.equalsIgnoreCase(other);

str.indexOf(text);

str.lastIndexOf(text);

str.replace(old,new);

str.split(",");

str.trim();

str.toUpperCase();

str.toLowerCase();

str.isEmpty();
```

---

# Frequently Used Utility Methods in DSA

```java
Arrays.sort(arr);

Arrays.binarySearch(arr,key);

Arrays.toString(arr);

Arrays.deepToString(matrix);

Collections.sort(list);

Collections.reverse(list);

Collections.max(list);

Collections.min(list);

Collections.frequency(list,x);

Math.max(a,b);

Math.min(a,b);

Math.abs(x);

Math.sqrt(x);

Math.pow(a,b);

Integer.parseInt(str);

Character.isDigit(ch);

Character.isLetter(ch);

Objects.equals(a,b);
```

---

# Quick Reference Table

| Class | Common Methods |
|-------|----------------|
| `Arrays` | `sort()`, `binarySearch()`, `fill()`, `copyOf()`, `equals()`, `toString()`, `deepToString()` |
| `Collections` | `sort()`, `reverse()`, `shuffle()`, `swap()`, `max()`, `min()`, `frequency()`, `binarySearch()` |
| `Math` | `sqrt()`, `pow()`, `max()`, `min()`, `abs()`, `random()`, `ceil()`, `floor()`, `round()` |
| `Integer` | `parseInt()`, `valueOf()`, `toString()`, `compare()` |
| `Character` | `isDigit()`, `isLetter()`, `isUpperCase()`, `isLowerCase()`, `toUpperCase()`, `toLowerCase()` |
| `Objects` | `equals()`, `hash()`, `requireNonNull()` |
| `String` | `length()`, `charAt()`, `substring()`, `contains()`, `replace()`, `split()`, `trim()`, `toUpperCase()`, `toLowerCase()` |

---

# Interview Tips 💡

- **`Arrays`** works only with **arrays**.
- **`Collections`** works with **Collection Framework objects** like `List`, `Set`, and `Queue`.
- `Arrays.sort()` is commonly used in array-based DSA problems.
- `Collections.sort()` is used for sorting `List` implementations.
- `Arrays.binarySearch()` and `Collections.binarySearch()` require the data to be **sorted**.
- Utility class methods are **static**, so you call them using the class name (e.g., `Arrays.sort(arr)`), not by creating an object.
- `java.lang` classes (`Math`, `String`, wrapper classes) are imported automatically; `java.util` classes (`Arrays`, `Collections`, `Objects`) require an import.