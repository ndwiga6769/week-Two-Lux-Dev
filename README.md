### Garbage Collection in Python

It is the process of automatically freeing up memory by removing objects
that are no longer referenced or in use. In Python, memory management is 
handled by the Python memory manager, which includes mechanisms like 
reference counting and a cyclic garbage collector.

Reference Counting:

Every object in Python has a reference count. 
When an object's reference count reaches zero (i.e., no variables 
or data structures point to it), it is automatically deallocated from memory.

Cyclic Garbage Collection: 

Python’s garbage collector can detect reference cycles, 
which happen when objects reference each other, preventing
their reference counts from reaching zero. The garbage collector
identifies these cycles and breaks them to free memory.

Garbage collection is crucial because it ensures efficient memory usage,
preventing memory leaks in long-running programs.

### Key Differences between NumPy Arrays and Python Lists

- Data Type: NumPy arrays have elements of a single data type, 
whereas Python lists can store elements of different types.

- Performance: NumPy arrays are faster for numerical computations 
because they use contiguous memory blocks and are optimized for 
numerical operations, while Python lists are less efficient as 
they store pointers to objects.

- Memory Efficiency: NumPy arrays use less memory compared to lists
because they store elements in a more compact form.

- Functionality: NumPy arrays come with a wide range of mathematical
and matrix operations that are not available with lists.

Advantages of NumPy Arrays:

Fast element-wise operations and broadcasting.
Support for multi-dimensional arrays and advanced mathematical functions.
Efficient memory usage and better performance in large-scale numerical computations.