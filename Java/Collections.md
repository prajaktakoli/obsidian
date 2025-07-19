
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
