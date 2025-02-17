# Cuckoo Hashing Data Structure

## Overview

This project implements a robust Cuckoo Hashing data structure designed to effectively handle and minimize collisions.

The Cuckoo Hash employs a dual-table approach and recursive eviction strategy.

## Key Mechanism

Keys are recursively evicted and reinserted into one of two hash tables until:

- A vacant spot is found in either table. (Hash table one or two)
- The hash tables dynamically expand in size.
- The Bit Hash hashing function is reset to avoid infinite loops.

## Other Characteristics

### Dynamic Scaling
- Automatically increases table size when necessary to accommodate more keys and avoid excessive collisions.

### Hashing Flexibility
- Utilizes a robust hashing mechanism (Bit Hash) that can be reset to improve distribution as needed.

### Testing
- Using `pytest`, the implementation is rigorously tested with large-scale insertions of up to **10,000 keys** at a time.
- These tests ensure the data structure maintains **functionality, efficiency, and correctness**, even under high-load scenarios.
