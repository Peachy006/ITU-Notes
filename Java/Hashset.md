# Java HashSet

## Overview
- **Implements:** `Set<E>` interface
- **Key property:** Stores **unique elements** (no duplicates)
- **Underlying structure:** Backed by a `HashMap`
- **Order:** **Unordered**, iteration order is not guaranteed (may change when elements are added/removed)
- **Nulls:** Allows at most one `null` element

---

## When to Use
- Need **fast lookups** (O(1) average for add, remove, contains)
- Need **uniqueness** of elements
- Don’t care about ordering of elements

---

## Key Methods
| Method               | Description                           |
| -------------------- | ------------------------------------- |
| `add(E e)`           | Adds element if not already present   |
| `remove(Object o)`   | Removes element if present            |
| `contains(Object o)` | Returns `true` if element exists      |
| `size()`             | Returns number of elements            |
| `isEmpty()`          | Checks if set is empty                |
| `clear()`            | Removes all elements                  |
| `iterator()`         | Returns iterator to traverse elements |

---

## Basic Example
```java
import java.util.HashSet;

HashSet<String> set = new HashSet<>();
set.add("Apple");
set.add("Banana");
set.add("Apple"); // Duplicate ignored

System.out.println(set.contains("Banana")); // true
set.remove("Apple");
System.out.println(set.size()); // 1











Iterating

for (String s : set) {
    System.out.println(s);
}

// OR
Iterator<String> it = set.iterator();
while (it.hasNext()) {
    System.out.println(it.next());
}













Tips

    For ordered sets, use:

        LinkedHashSet → maintains insertion order

        TreeSet → keeps elements sorted

    HashSet operations depend on hashCode() and equals() of elements:

        Ensure these methods are correctly overridden in custom classes.

Related Classes

    LinkedHashSet – preserves insertion order

    TreeSet – keeps elements in natural or custom order

    Guava Multiset – allows duplicates (not part of standard Java)