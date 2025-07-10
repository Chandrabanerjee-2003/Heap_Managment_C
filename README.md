# Heap Management System 

This project presents a custom heap memory management system in C, built using the Buddy Allocation Algorithm. It emulates a basic yet effective memory allocator, similar to those used in operating systems, designed to manage dynamic memory requests efficiently through splitting and coalescing memory blocks.

## Features

- **Buddy System Allocation**: Memory is allocated in blocks sized as powers of two. The allocator uses a recursive divide-and-conquer strategy for splitting large blocks and a merging strategy to reclaim fragmented space.
- **Real-Time Allocation & Freeingn**:The system handles dynamic memory requests interactively. Users can allocate and deallocate memory through the command-line interface.
- **Free and Allocated Lists**: Maintains and displays separate linked lists for free and allocated memory blocks, allowing users to view the current state of memory at any point.
- **Lightweight Overhead**: Each block carries minimal metadata (such as block size, status, and linkage), ensuring space efficiency while managing memory structure.

## Core Data Structures

- `Block Structure` (struct contains)
  - `Size`:Indicates the size of the block
  - `is_free`:Boolean flag for allocation status
  - `next`:Pointer to the next block in the list
- `Memory Management` 
  - Free list is maintained as a linked list of blocks.


## File Overview

- `new3.c`: Main source code file that contains the full implementation of the heap management logic.

## Build Instructions

### Requirements
- GCC or any standard C compiler.

### Compilation
```bash
gcc -o heap_manager heap_management.c

