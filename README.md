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


### List Comprehension in Python

List comprehension provides a concise way to create lists.
It allows for constructing lists by embedding a for-loop 
inside square brackets, optionally with conditions

         List comprehension to generate squared values

        squares = [x**2 for x in range(10)]
        print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

        List comprehension with a condition to filter even numbers

        evens = [x for x in range(10) if x % 2 == 0]
        print(evens)  # Output: [0, 2, 4, 6, 8]

### Shallow and Deep Copying in Python

Shallow Copy: A shallow copy creates a new object, but the elements inside the 
object are still references to the original. This means changes to mutable objects
within the shallow copy will reflect in the original object

Deep Copy: A deep copy creates a new object and recursively copies all objects 
inside, so the new copy is completely independent of the original.

        Use shallow copy when you only need to copy the outer object 
        (and the internal objects can remain shared).
        Use deep copy when you need an entirely independent copy, including all nested objects

        
        Original list with nested structure
        original = [[1, 2], [3, 4]]

        Shallow copy
        shallow = copy.copy(original)
        shallow[0][0] = 100
        print(original)  # Output: [[100, 2], [3, 4]] (modifies original)

        Deep copy
        deep = copy.deepcopy(original)
        deep[0][0] = 1
        print(original)  # Output: [[100, 2], [3, 4]] (original remains unchanged)


### Difference between Lists and Tuples in Python

Mutability: Lists are mutable, meaning you can modify (add, remove, change) 
their elements after creation. Tuples are immutable, meaning once they 
are created, their elements cannot be changed.

Syntax: Lists are created using square brackets [ ], while 
tuples are created using parentheses ( ).

Performance: Tuples are generally faster than lists because they are 
immutable and thus require less memory.

Use Case: Lists are used when data needs to be changed or modified, 
whereas tuples are used for fixed collections of items, such as 
constants or grouped data that should not change.

            List
            lst = [1, 2, 3]
            lst[0] = 10  # This works because lists are mutable
            print(lst)  # Output: [10, 2, 3]

            Tuple
            tup = (1, 2, 3)
            # tup[0] = 10  # This would raise an error because tuples are immutable
            print(tup)  # Output: (1, 2, 3)

