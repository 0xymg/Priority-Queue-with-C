# Priority Queue Implementation in C

This project demonstrates a robust implementation of a **Priority Queue** using the C programming language. It focuses on efficient data management, custom prioritization logic, and the practical application of abstract data types (ADTs) in a real-world scenario.

## Core Objective

The primary goal of this project is to implement a flexible and efficient **Priority Queue** and **Stack** architecture. The codebase showcases:
- **Custom Insertion Logic**: Maintaining a sorted list based on multiple priority levels without full-list sorting.
- **Dynamic Memory Management**: Manual allocation and reallocation of memory for nodes and stacks.
- **Abstract Data Type (ADT) Design**: Using structs and enums to create a modular and reusable data structure.

## Example Application: Flight Seat Management

To demonstrate the priority queue in action, the project includes a **Flight Seat Management System**. In this example:
- **Primary Priority**: Ticket class (Business > Economy > Standard).
- **Secondary Priority**: Special status within a class (e.g., Diplomats in Business, Veterans in Economy).
- **Resource Management**: Stacks are used to represent physical seats being "popped" and assigned to the highest-priority individuals in the queue.

## Data Structure Details

### Priority Queue (Linked List)
- **Node-based**: Each passenger is a node in a linked list.
- **O(N) Insertion**: The `pushque` function traverses the list to find the correct position based on the hierarchical priority rules, ensuring the head is always the next in line.

### Stack
- **Array-based**: Used for managing available seat "tokens" for different flight classes.
- **Dynamic Growth**: Supports reallocation if the capacity needs to expand during runtime.

## Supported Commands (Example Interface)

The implementation processes a command-driven interface via file I/O:
- `addseat`: Initialize or add resources (seats) to the stacks.
- `enqueue`: Add an element to the priority queue with specific priority metadata.
- `sell`: Dequeue the highest-priority elements and match them with available stack resources.
- `report` & `close`: State inspection and cleanup of the data structures.

## Getting Started

### Compilation

```bash
gcc main.c -o priority_queue_demo
```

### Usage

```bash
./priority_queue_demo input.txt output.txt
```

## Implementation Highlights

- **Hierarchical Logic**: Implementation of complex business rules (e.g., "Diplomats first in Business, then everyone else in Business, then Veterans in Economy...").
- **Pointer Arithmetic**: Extensive use of double pointers (`passenger** head`) for in-place list modification.
- **Cleanup**: Modular functions for popping and freeing memory to prevent leaks.

## License

This project is open-source and available under the MIT License.
