# Cpp notes

## OOPS Concepts
Object Oriented Programming is a paradigm that provides everything is represented as an objects.
Smalltalk is considered as the first truly object-oriented programming language.
4 Main Pillars of OOPS are:-
1. Abstraction,
2. Encapsulation,
3. Inheritance,
4. Polymorphism,

-------:Abstraction:--------
Abstraction is the process to hide the internal details and showing only functionality.
Abstraction can be achieved by using Abstract Class and Interface.
##Abstraction is selection of relevant data/information for one particular object of intent.
Abstraction can be achieved by two ways:
-->Abstract class
-->Interface

-------:Encapsulation:------
-->The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must:
declare class variables/attributes as private provide public get and set methods to access and update the value of a private variable.
-->Binding (or wrapping) code and data together into a single unit is known as encapsulation.
##protecting the data from outside interferance.

-------:Inheritance:--------
-->When one object acquires all the properties and behaviours of parent object i.e. known as inheritance. 
-->It provides code reusability.
##generalization to specialization.
##creating new type from existing type.

-------:Polymorphism:--------
When one task is performed by different ways i.e. known as polymorphism. 
For example: to convince the customer differently, to draw something e.g. shape or rectangle etc.
- One interface multiple implementation
- when single object is exist in differenet forms in different situation.
Let's consider a real-life example of polymorphism. A lady behaves like a teacher in a classroom, mother or daughter in a home
and customer in a market. Here, a single person is behaving differently according to the situations.
Polymorphism can be achieved in two ways;
1. static polymorphism
2. dynamic polymorphism

Class & Objects:-
A class is a logical entity, while an object is a physical entity. 
A class does not allocate memory space; on the other hand, an object allocates memory space.

Object:
A object is an instance of class.
Any entity that has state and behavior is known as an object. 
For example: chair, pen, table, keyboard, bike etc. It can be physical and logical.

Class:
Its a type (which type abstract type);
Collection of objects is called class. It is a logical entity.
A class is a blueprint for creating objects.
Example- Take the class of cars as an example. Even if different names and brands may be used for different cars, 
all of them will have some characteristics in common, such as four wheels, a speed limit, a range of miles, etc. 
In this case, the class of car is represented by the wheels, the speed limitations, and the mileage.


## Types of inheritance

Single inheritance
Multiple inheritance
Multilevel inheritance
Hybrid inheritance
Hierarchical inheritance

## POINTERS:
Pointers are used to store and maintain the addresses of memory blocks that are dynamically allocated.

int val=20;					val  = 20
int* ptr=&val;				&val = address of 20
							ptr  = address of 20
							*ptr = 20              // Access the memory address of val and output its value.
							
			nums[i] is equivalent to *(nums+i)
In general, nums[ i ][ j ] is equivalent to *(*(nums+i)+j) 
function pointer - used in callback function

Void Pointer-->
A void pointer is a pointer which is having no datatype associated with it. It can hold addresses of any type.

callback function-->
It is a function that is passed as an argument to another function and is called by that function at a later time. 

Binding
1. call back function
2. passing fun as an argument to another funct.

Dangling pointer is a pointer that points to memory that is no longer valid.
-->undefined behaviour
Examples:

int *ap[2]					(-- array pointer)
int (*padd)(int a, int b);   (---function pointer)
int (*pa)[2]; 				(------pointer to an array)

int *ap[2]; array to pointer


step 1.		int i;				int a[2];

step 2.		int (i);			int (a)[2];

step 3.	replace identifier with pointer identifier

			int (*pi);			int (*pa)[2];

step 4.	remove brackets if nothing on right hand side on original identifier. otherwise keep brackets.

			int *pi;			int (*pa)[2];
   
-------------------------------------------------------------------------------------------------------
int add(int a, int b)

int (add)(int a, int b);

int (*padd)(int a, int b);

int (*padd)(int a, int b); 

=========================================================================================================
## Constructor:

constructor can not be inherited
destructor can be inherited
copy constructor = constructor with a referenece parameter

allias- referencing as a same name

Type demotion - only c/c++
Type pormotion - all language

overriding - redefined of base class func. in its derieved class with same signature.

overloading- same func with same name;

operator overloading- when we use  existing operators on objects

==========================================================================================================
Call By Value:
In call by value, value being passed to the function is locally stored by the function parameter in stack memory location.

Call By Reference:
In call by reference, original value is modified because we pass reference (address).


------------------------------------------------------------
## Exception Handeling:

An exception is an unwanted or unexpected event, which occurs during the execution of a program 
i.e at run time, that disrupts the normal flow of the program’s instructions.

There are two types of exceptions:
a) Synchronous,   -->one process depend on other
b) Asynchronous   -->No dependency

Exception Handeling
domain_error 		Domain error occurred.
invalid_argument 	Invalid argument used in function call.
length_error 		An attempt was made to create an object that was too large.
out_of_range 		An argument to a function was not in the required range.

The following run-time exceptions are derived from the base class runtime_error.

overflow_error 		Arithmetic overflow occurred.
range_error 		An internal range error occurred.
underflow_error 	An underflow occurred.

---------------------------------------------------------------------------------------
## File Handelling:-

File Handling stands for the manipulation of files storing relevant data using a programming language.
File handling is the process of reading from and writing to files on disk.
Two main types of files in C++:
1. text files
2. binary files

fstream
1. ofstream-->	Creates and writes to files
2. ifstream-->	Reads from files

why file handelling ?
 Whenever we execute a program, it gets loaded into the main memory, and all data required for the
 program also exists in the main memory. But in real-world programming, manipulation exists on a 
 large data set (typically in GigaBytes), so we will not store all data on Main Memory. 
 The extensive data remains stored on disk, and through a stream, we bring only a particular set of 
 data that the program needs now.
 
 For achieving file handling we need to follow the following steps:-
 STEP 1-Naming a file
 STEP 2-Opening a file
 STEP 3-Writing data into the file
 STEP 4-Reading data from the file
 STEP 5-Closing a file.

 
-----------------------------------------------------------------------------------------

What is Reference?
A reference is a variable that is referred to as another name for an already existing variable. 
The reference of a variable is created by storing the address of another variable.

What Is Pointer?
A pointer is a variable that contains the address of another variable. 
It can be dereferenced with the help of (*) operator to access the memory location to which the pointer points.

-------------------------------------------------------------------------------------------------

Shallow copy -- refrence copy
Deep copy -- value to value

-------------------------------------------------------------------------------------------------
## variadic functions:-
function that can take a variable number of arguments
1. When the data type of all the arguments is the same
2. When the data type of all the arguments is different.


local value - stack
global value/global function - function area

stack- automatic flush
heap- my responsiblity to flush


node *head  
it means head is a pointer which shall store address of any object of type node,
we know address are unsigned long, so pointers are always allocated 4 or 8 bytes 
of memory irrespected of its type.
here head will not be allocated memory for info and next.

		+------------------------------+
		|  node *newnode = new node(); |
		+------------------------------+


Friend Function - non member function 
function signature - Function name + return type

struct-  instance are pass by value
class-   instance pass by reference

===========================================================================================================
## Inheritance:

DEFAULT
BY default every thing is inherited as private 
ie. all base class members becomes private member of derived class.

PROTECTED
if inherited as protected 
ie. all base class members becomes protected and can be used only inside
the derived class member of derived class not outside it, private & protected
members of base class maintain their access specifier but public members of base class becomes protedted.

PUBLIC
if inherited as public 
ie. all base class members maintain its accessbility, there is no change in accessibility.

======================================================================================================================


Early binding (also called static binding or compile-time binding).
Late binding (also called dynamic binding or runtime binding).

virtual function
-----> a member function of a class that can be overridden in a derived class.

We cannot have a virtual constructor, but we can have a virtual destructor.

int main() --- return status of execution

Functions always return something.
order of constructor- parent to child
order of destructor - reverse of constructor

virtual class  - to solve daimond problem
				       - to remove ambiguity in hybrid inheritence.
				
Virtual function--> is a member function that is declared within the base 
				class and can be redefined by the derived class.


Pure Virtual Function-->
The "do-nothing" function is known as a pure virtual function. 
A pure virtual function is a function declared in the base class that has no definition relative to the base class.


#compile-time polymorphism is achieved by overloading functions and operators. 
#Run-time polymorphism is accomplished by using inheritance and virtual functions.

C++ ---> unary operators such as new and delete	---> allocating and freeing the memory.

Binding->to the process of associating a function call with the appropriate function definition
		 at compile-time or run-time.

Early binding/static binding/compile-time binding,---- at compile-time.faster execution.
Late binding/dynamic binding/run-time binding--------  at run-time.
				
why we override ?
1. To provide a more specific implementation: 
2. To customize behavior: 
3. To implement polymorphism:
method overriding is an important concept in object-oriented programming 
that allows us to create more flexible and customizable code.
interface - which interacting with data 

constructors not be virtual
destructor can be virtual
pure virtual function - override 

virtual functions are implemented using a mechanism called the virtual method table (VMT), 
also known as the virtual function table (VFT) or the virtual table (Vtable).

why we use virtual function
virtual functions are used to achieve polymorphism, which is the ability of objects of 
different classes to be treated as if they were objects of the same class type.


--> endl inserts a newline character and flushes the output buffer, 
--> \n only inserts a newline character.

---------------------------------------------------------
## C++ Templates:--
It allows you to define the generic classes and generic functions.
Function templates
Class templates


										C++ STL(Standard Tag Library)
													|
								+---------------------------------------------------------+
							Containers													Algorithm
								|														|
								|														+->Binary Search
+-----------------------+-----------------------+-------------------------------+		|
|						|						|								|		+->Lower/Upper bound
Sequence Containers	Containers Adapters	 Associative Containers	Unordered Associative	+->min/max
|					|					 |						|						+->reverse/rotate
|					|					 |						|						+->sort/swap etc
Arrays				Stack				 Set					Unordered Set					
Vector				Queue				 Map					Unordered Map					
Deque				Priority Queue		 MultiSet*				Unordered MultiSet*				
List									 MultiMap*				Unordered MultiMap*			
forward_list*

==============================================================================================================
Interface --- help in Loose Coupling


To Sort-->
sort(__.begin(),__.end());

To print/Iterate-->
for(vector<int>::iterator itr=__.begin(),itr!=__.end();i++){
cout<<*itr;
}

Iterator 		Access Allowed
Random 			Access Store and retrieve values. Elements may be accessed randomly.
Bidirectional 	Store and retrieve values. Forward and backward moving.
Forward 		Store and retrieve values. Forward moving only.
Input 			Retrieve, but not store values. Forward moving only.
Output 			Store, but not retrieve values. Forward moving only.


collision- 	when duplicated key generates
probing-	we do probing when collision occurs


array length in c++ -   	 sizeof(arr)/sizeof(int);
array length in java & c#-   arr.length;

string length in java-  str.length();
string length in c++-   str.length(); & int size = str.size();

string size = str.size();
for lowercase to uppercase			newstr = toupper(str);
for uppercase to lowecase			newstr = tolower(str);

Iterators in C++ STL:
-->Iterators are used to point at the memory addresses of STL containers.

begin() :- This function is used to return the beginning position of the container.
end() :- This function is used to return the after end position of the container.
advance() :- This function is used to increment the iterator position till the specified number mentioned in its arguments.
next() :- This function returns the new iterator that the iterator would point after advancing the positions mentioned in its arguments.
prev() :- This function returns the new iterator that the iterator would point after decrementing the positions mentioned in its arguments.
inserter() :- This function is used to insert the elements at any position in the container. It accepts 2 arguments, the container and iterator to position where the elements have to be inserted.


Vector:
-->Vectors are same as dynamic arrays.
-->Vector elements are placed in contiguous storage so that they can be accessed and traversed using iterators.
vector<int> iv; 			// create zero-length int vector
vector<int> v(5); 			// create 5-element int vector
vector<char> cv(5, 'x'); 	// initialize a 5-element char vector
vector<int> iv2(iv); 		// create int vector from an int vector

Fuctions:
begin() – Returns an iterator pointing to the first element in the vector.
end() – Returns an iterator pointing to the theoretical element that follows the last element in the vector.
size() – Returns the number of elements in the vector.
capacity() – Returns the size of the storage space currently allocated to the vector expressed as number of elements.
empty() – Returns whether the container is empty.
push_back() – It push the elements into a vector from the back.
pop_back() – It is used to pop or remove elements from a vector from the back.
insert() – It inserts new elements before the element at the specified position.
erase() – It is used to remove elements from a container from the specified position or range.
swap() – It is used to swap the contents of one vector with another vector of same type and size.
clear() – It is used to remove all the elements of the vector container.
emplace() – It extends the container by inserting new element at position.
emplace_back() – It is used to insert a new element into the vector container, the new element is added to the end of the vector.


List:
-->Lists are sequence containers that allow non-contiguous memory allocation.
-->List in C++ STL implements a doubly linked list.
-->For implementing a singly linked list, we can use forward_list class in C++ STL.

Functions:-
front() – Returns the value of the first element in the list.
back() – Returns the value of the last element in the list.
push_front(g) – Adds a new element ‘g’ at the beginning of the list.
push_back(g) – Adds a new element ‘g’ at the end of the list.
pop_front() – Removes the first element of the list, and reduces the size of the list by 1.
pop_back() – Removes the last element of the list, and reduces the size of the list by 1.
begin() and end() – begin() function returns an iterator pointing to the first element of the list.
empty() – Returns whether the list is empty(1) or not(0).
insert() – Inserts new elements in the list before the element at a specified position.
reverse() – Reverses the list.
size() – Returns the number of elements in the list.
sort() – Sorts the list in increasing order.


Heap:
-->Tree-based data structure
-->used to implement priority queues
-->A Heap is a complete tree (All levels are completely filled except possibly the last 
	level and the last level has all keys as left as possible).
-->A Heap is either Min Heap or Max Heap.
-->min heap, the parent node has a smaller value than its children,
-->max heap, the parent node has a larger value than its children.
-->The root node of a min heap has the smallest value in the heap, 
	while the root node of a max heap has the largest value in the heap.
-->Heaps are commonly used in algorithms such as heap sort, Dijkstra's algorithm, and Prim's algorithm 
	for finding the shortest path and minimum spanning tree in a graph.

Stack:
-->Stack is a linear data structure.
-->LIFO(Last In First Out) or FILO(First In Last Out).
-->Basic 4 operations:- Push	Pop		Peek/Top	isEmpty
--> Using STL Class Implementation:
	empty() 	– Returns whether the stack is empty.
	size() 		– Returns the size of the stack.
	top() 		– Returns a reference to the topmost element of the stack.
	push(g) 	– Adds the element ‘g’ at the top of the stack.
	pop() 		– Deletes the topmost element of the stack.
	(All of the above functions work in O(1) time complexity)

Hashing:
-->Hashing is a method of storing and retrieving data from a database efficiently.
-->Hasing implement in STL
	-set
	-unordered_set
	-map
	-unordered_map
	
Set:
-->Associative containers.
-->Each element has to be unique.
-->Elements stored in Ordered way.
-->T.C - 0(Log n)
-->Element cannot be modified once it is added.
-->Some basic functions associated with Set:
	begin() 	– Returns an iterator to the first element in the set.
	end() 		– Returns an iterator to the theoretical element that follows last element in the set.
	size() 		– Returns the number of elements in the set.
	insert(val) – Inserts a new element val in the Set.
	find(val) 	- Returns an iterator pointing to the element val in the set if it is present.
	empty() 	– Returns whether the set is empty.

Unordered Set	- Not in order ,Unique keys/elements, T.C-O(1).

Map:
-->Map container is also associative and stores elements in an ordered way.
-->store sorted key-value pair, in which each key is unique.
-->It can be inserted or deleted but cannot be altered.
-->Use key to iterate.
-->key should be int(recommended).
-->Some basic functions associated with Map:
	begin() 					– Returns an iterator to the first element in the map.
	end() 				– Returns an iterator to the theoretical element that follows last element in the map.
	size() 						– Returns the number of elements in the map.
	empty() 					– Returns whether the map is empty.
	insert({keyvalue, mapvalue})– Adds a new element to the map.
	erase(iterator position) 	– Removes the element at the position pointed by the iterator
	erase(const g)				– Removes the key value ‘g’ from the map.
	clear() 					– Removes all the elements from the map.


Map - store in order way  , T.C- O(Log n)
Unordered Map - T.C- O(1), 	
Hashmap	- 	auto key generated by HashFunction
