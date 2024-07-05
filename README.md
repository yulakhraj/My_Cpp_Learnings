# C++ Notes

## OOP Concepts

Object-Oriented Programming (OOP) is a paradigm that represents everything as objects. Smalltalk is considered the first truly object-oriented programming language. The four main pillars of OOP are:

1. Abstraction
2. Encapsulation
3. Inheritance
4. Polymorphism

### Abstraction

Abstraction is the process of hiding internal details and showing only functionality. It can be achieved using Abstract Classes and Interfaces. It involves selecting relevant data/information for a particular object.

### Encapsulation

Encapsulation ensures that "sensitive" data is hidden from users by declaring class variables/attributes as private and providing public getter and setter methods to access and update the value of a private variable. It binds code and data together into a single unit.

### Inheritance

Inheritance allows one object to acquire all properties and behaviors of a parent object, promoting code reusability. It generalizes to specialization and allows creating new types from existing types.

### Polymorphism

Polymorphism allows one task to be performed in different ways. It can be achieved through static polymorphism (function overloading) and dynamic polymorphism (using inheritance and virtual functions). A real-life example is a person behaving differently in various situations, such as a teacher in a classroom or a customer in a market.

## Classes & Objects

A class is a blueprint for creating objects, which are instances of classes. Objects have state and behavior, such as a chair or bike.

## Types of Inheritance

1. Single inheritance
2. Multiple inheritance
3. Multilevel inheritance
4. Hybrid inheritance
5. Hierarchical inheritance

## Pointers

Pointers store and maintain the addresses of memory blocks that are dynamically allocated.

- `int val = 20;` (value = 20)
- `int* ptr = &val;` (ptr holds the address of val)

Function pointers are used in callback functions. A void pointer can hold addresses of any type.

### Dangling Pointer

A dangling pointer points to memory that is no longer valid, leading to undefined behavior.

### Examples

- `int *ap[2]` (array pointer)
- `int (*padd)(int a, int b);` (function pointer)
- `int (*pa)[2];` (pointer to an array)

## Constructor

- Constructors cannot be inherited.
- Destructors can be inherited.
- Copy constructors have a reference parameter.

## Exception Handling

Exceptions are unwanted or unexpected events occurring during program execution, disrupting the normal flow. They can be synchronous or asynchronous.

### Common Exceptions

- `domain_error`
- `invalid_argument`
- `length_error`
- `out_of_range`
- `overflow_error`
- `range_error`
- `underflow_error`

## File Handling

File handling involves reading from and writing to files on disk, crucial for manipulating large data sets.

### Steps for File Handling

1. Naming a file
2. Opening a file
3. Writing data to the file
4. Reading data from the file
5. Closing the file

## References vs. Pointers

- A reference is another name for an existing variable, created by storing the address of another variable.
- A pointer contains the address of another variable and can be dereferenced to access the memory location.

## Shallow vs. Deep Copy

- Shallow copy: reference copy
- Deep copy: value to value copy

## Variadic Functions

Functions that can take a variable number of arguments, useful when data types are the same or different.

## Inheritance Access Specifiers

- **Default**: Inherited as private.
- **Protected**: Inherited as protected; public members of the base class become protected.
- **Public**: Inherits accessibility as-is.

## Early vs. Late Binding

- **Early binding** (static/compile-time): Faster execution, associated at compile-time.
- **Late binding** (dynamic/run-time): Associated at run-time.

## Virtual Functions

Virtual functions are member functions that can be overridden in derived classes, enabling polymorphism. They are implemented using a virtual method table (VMT).

### Pure Virtual Function

A pure virtual function is declared in the base class without a definition, requiring derived classes to override it.

## C++ Templates

Templates allow defining generic classes and functions.

- Function templates
- Class templates

## C++ STL (Standard Template Library)

```plaintext
C++ STL (Standard Template Library)
           |
+--------------------------+
Containers                Algorithm
    |                        |
    |                        +-> Binary Search
+------------+               |
|            |               +-> Lower/Upper bound
Sequence Containers       +-> min/max
|            |               +-> reverse/rotate
|            |               +-> sort/swap etc
Arrays    Container Adapters  Associative Containers     Unordered Associative Containers
|            |                   |                        |
|            |                   |                        |
Vector     Stack                Set                      Unordered Set
Deque      Queue                Map                      Unordered Map
List       Priority Queue       MultiSet*                Unordered MultiSet*
forward_list*                   MultiMap*                Unordered MultiMap*
