
# 21. Core Collection Interfaces

| Interface | Description                         | Common Implementations           |
| --------- | ----------------------------------- | -------------------------------- |
| `List`    | Ordered, indexed, allows duplicates | ArrayList, LinkedList, Vector    |
| `Set`     | No duplicates, unordered or sorted  | HashSet, LinkedHashSet, TreeSet  |
| `Map`     | Key-value pairs, keys unique        | HashMap, TreeMap, LinkedHashMap  |
| `Queue`   | FIFO or priority-based collection   | Queue, PriorityQueue, LinkedList |
## 🔸 List Interface

- Ordered collection (indexed)
- Allows duplicate elements
- Can access by position (`get(index)`)

## Set Interface

- No duplicate elements
- Does **not guarantee order**
- Useful for unique values

### ✅ Example:

`Set<Integer> set = new HashSet<>(); set.add(10); set.add(20); set.add(10); // Ignored`

## 🔸 Map Interface

- Stores **key-value pairs**
- Keys must be unique
- Can return keySet(), values(), entrySet()
- 
```
Map<Integer, String> map = new HashMap<>();
map.put(1, "A");
map.put(2, "B");
map.put(1, "C"); // Overwrites key 1
```

## Queue Interface

- Based on **FIFO** (First In First Out)
    
- Used for tasks, messaging
    
- Methods: `offer()`, `poll()`, `peek()`
```
Queue<String> q = new LinkedList<>();
q.offer("Task1");
q.offer("Task2");
q.poll(); // Removes "Task1"
```

---

## 23. Map Implementations in Java

| Class           | Ordering          | Null Keys | Null Values | Internal DS      | Thread-safe |
| --------------- | ----------------- | --------- | ----------- | ---------------- | ----------- |
| `HashMap`       | ❌ Unordered       | ✅ 1 key   | ✅ multiple  | Hash Table       | ❌ No        |
| `LinkedHashMap` | ✅ Insertion       | ✅ 1 key   | ✅ multiple  | Hash Table + DLL | ❌ No        |
| `TreeMap`       | ✅ Sorted (by key) | ❌ No      | ✅ Yes       | Red-Black Tree   | ❌ No        |

---
## 🔍 HashMap

- Unordered
- Allows **one null key**, many null values
- Key is hashed → bucket → linked list (or tree if many collisions)

```java
Map<String, Integer> map = new HashMap<>();
map.put("Java", 90);
map.put(null, 50);
System.out.println(map.get(null)); // 50
```
## LinkedHashMap

- Maintains **insertion order**
- Slightly slower than HashMap


```
Map<String, String> linked = new LinkedHashMap<>(); 
linked.put("A", "Apple"); linked.put("B", "Banana");
```