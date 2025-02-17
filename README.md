# Cuckoo Hashing Data Structure

## Overview

This project implements a **robust Cuckoo Hashing** data structure designed to **effectively handle and minimize collisions**.

Cuckoo Hashing employs a **dual-table approach** with a **recursive eviction strategy**, ensuring efficient key insertions and lookups.

---

## Cuckoo Hashing Mechanism

Keys are recursively evicted and reinserted into one of two hash tables until one of the following conditions is met:

1. **A vacant spot is found** in either **Hash Table 1** or **Hash Table 2**.  
2. **The hash tables dynamically expand** to accommodate more keys.  
3. **The Bit Hash hashing function is reset** to prevent infinite loops.  

---

## Key Features

### 🔹 Dynamic Scaling  
- **Automatically increases table size** when necessary to accommodate more keys and prevent excessive collisions.  

### 🔹 Hashing Flexibility  
- Uses the **Bit Hash hashing mechanism**, which can be **reset dynamically** to enhance key distribution and avoid clustering.  

### 🔹 Rigorous Testing  
- **Pytest** is used to validate performance and correctness.  
- The implementation is **stress-tested** with large-scale insertions of **up to 10,000 keys** at a time.  
- Ensures the data structure remains **functional, efficient, and accurate** under high-load scenarios.  

---

## Running Tests

To run the test suite using `pytest`:

```sh
pytest cuckoo_hash_tests.py
