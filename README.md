# Dynamic Memory Reallocation using realloc() in C

## Overview

This project demonstrates how to use the `realloc()` function in C to resize dynamically allocated memory. The program first allocates memory using `malloc()` and then increases the allocated memory size using `realloc()`.

---

## Concepts Covered

- Dynamic Memory Allocation
- `malloc()`
- `realloc()`
- Pointers
- Memory Management
- Runtime Memory Allocation

---

## Project Description

The program performs the following operations:

1. Allocates memory for **4 integer elements** using `malloc()`.
2. Prints the allocated memory size and memory address.
3. Resizes the allocated memory to store **6 integer elements** using `realloc()`.
4. Prints the new memory size and updated memory address.

---

## Initial Memory Allocation

```c
size = 4 * sizeof(*ptr1);
ptr1 = malloc(size);
```

This allocates memory for:

```text
4 integers × 4 bytes = 16 bytes
```

---

## Memory Reallocation

```c
size = 6 * sizeof(*ptr1);
ptr2 = realloc(ptr1, size);
```

This resizes the memory block to:

```text
6 integers × 4 bytes = 24 bytes
```

`realloc()` may:

- Expand the existing memory block.
- Move the data to a new memory location if needed.
- Preserve the existing data during reallocation.

---

## Memory Illustration

### Before realloc()

```text
ptr1

+----+----+----+----+
|    |    |    |    |
+----+----+----+----+

Total Size = 16 Bytes
```

### After realloc()

```text
ptr2

+----+----+----+----+----+----+
|    |    |    |    |    |    |
+----+----+----+----+----+----+

Total Size = 24 Bytes
```

---

## Sample Output

```text
16 bytes allocated at address 0x55c3f0a8b2a0
24 bytes reallocated at address 0x55c3f0a8b2a0
```

**Note:** The memory address may remain the same or change depending on the availability of contiguous memory.

---

## malloc() vs realloc()

| malloc() | realloc() |
|----------|-----------|
| Allocates new memory | Resizes existing memory |
| Previous data does not exist | Existing data is preserved |
| Takes one size argument | Takes pointer and new size |
| Used for initial allocation | Used for resizing memory |

---

## Learning Outcomes

- Understanding dynamic memory allocation
- Using `malloc()` for memory allocation
- Using `realloc()` for resizing memory
- Working with pointers
- Managing memory efficiently at runtime

---

## Real-World Applications

- Dynamic Arrays
- Resizable Buffers
- Data Structures
- Embedded Systems
- Database Systems
- Memory Management Utilities

---

## Time Complexity

```text
O(1) Average Case
```

The actual complexity depends on whether memory needs to be moved during reallocation.

---

## Space Complexity

```text
O(n)
```

Where `n` is the size of the dynamically allocated memory.

---

## Key Takeaway

`realloc()` allows a program to resize dynamically allocated memory without losing existing data, making it useful for building flexible and memory-efficient applications.

---

## Author

**Amrutha D N**

```
