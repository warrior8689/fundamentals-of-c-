# fundamentals-of-cpp
Structure in c++

•To define a structure, we use the struct keyword, which allows grouping data members and member functions into a single user-defined type. 
Variables can be declared without repeating the struct keyword. .
Structures are used to build linked lists and trees and to represent real-world

Memory Layout of c++ program and size of structure

•the memory layout of a C++ program shows how various parts (like code, stack, heap, and data) are organized in memory during execution. Understanding it helps manage memory efficiently and avoid issues like leaks and stack overflow

Data size int a 2 float b 4 char c 1

Nested structure

•Nested structure is a structure that contains another structure as its member.

Advantages

•Code is cleaner ✔ Data organization is better ✔ Can easily represent real-life entities

pointer & array inside struct

•Pointers in C++ are variables that store the address of another variable while arrays are the data structure that stores the data in contiguous memory locations. In C++, we can manipulate arrays by using pointers to them. 

c++ pointer Arithmetic

•In C++, pointer arithmetic means performing valid arithmetic operations such as incrementing a pointer and decrementing a pointer on pointer variables to move and access memory locations efficiently.

Memory representation of structure with pointers

•In C++, the memory representation of a structure with pointers involves contiguous memory for the structure itself, where any pointer members inside it store the memory addresses of other data locations, which may or may not be contiguous with the structure's memory.

Linked list using array

•In order to convert an array to a linked list, start by defining a reference point. In this case, try to fix the start of the array, which will be the head of the linked list. After fixing the head, iterate through the entire array, convert every element into a node of the linked List, and keep linking them.  

pointer to structure

•Pointer to structure in C NAD C++ can also be referred to as Structure Pointer. A structure Pointer in C and C++ is defined as the pointer which points to the address of the memory block that stores a structure

Array + Pointer concept

•Array is stored in continuous block in the memory and the name of the array is the address of the first element. Pointer arithmetic gives the address of the next element (a+1, a+2).

Linked list + Traversal

•The concept of linked list is explained using a self-referential structure. The data in the structure is accessed and traversed with the help of a pointer and a loop

pass by value vs pass by reference in c

Pass by Value

•In pass by value, the function receives a copy of the variable's value.

Any changes made to the parameter inside the function do not affect the original variable in the caller. Two separate copies exist in memory: The original variable in the caller and the function's local copy

•pass by refrence

n pass by reference, the function receives the address of the variable instead of a copy.

The function can directly modify the original variable in the caller. Only one memory location exists for the variable, so changes inside the function affect the original variable. In C, this is done using pointers, as C does not have pass by reference like C++. Instead, you can pass the address of a variable to a function using pointers.

how structure value change when passed by pointer

•When a structure is passed by pointer to a function (often referred to as "pass by reference" in this context), any modifications made to the structure's members inside the function will change the original structure's values in the calling function.

pointer increment on string

•When you increment a pointer, the address it stores increases by the size of the data type it points to. For a char* pointer, the data type is a char, which is defined as being one byte in size. Thus, pointer++ moves the pointer to the memory address of the next character in the sequence. This mechanism allows for efficient iteration through a string, as the characters are stored in contiguous memory locations and the string is terminated by a null character (\0).

•Pre increment and Post increment..

The logic of Pre-increment and Post-increment: ++(p++)->c Concept: Here, p++ is a post-increment operation, meaning the old value is used first before the pointer moves forward.

Step: Initially, the pointer p is at address 1000.

During p++, the pointer moves to address 1004, but the expression uses the old address (1000) for the current operation. The ->c operator fetches the value (e.g., 2000) from that specific address. The outer pre-increment (++) then increments that fetched value, changing it to 2001.

Pointer with structure

•Pointer with Structure: *++p->cConcept: Here -> has higher priority than *. Step: First p->c is resolved, then incremented and dereferenced. diagream show the value is fetched from address 4000 and the pointer is jumped to the next memory block.

Strings and Memory: char *str[]

•Here is the concept of an Array of Pointers to Strings.

sizeof(str): Returns the size of the entire array. If the array contains 5 pointers, each pointer being 2 bytes long (using older systems), the output will be 10
                                          Note: On modern 64-bit systems, a pointer is 8 bytes long, so this will return 40. Your notes are based on a 16-bit compiler (such as Turbo C).            sizeof(str[0]): Returns the size of the first element (a pointer) of the array, which is 2.
