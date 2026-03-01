CS 210: Item Frequency Counter (C++)
Project Summary

This project is a C++ console application that reads a list of grocery items from an input file and calculates how many times each item appears. The program stores the results using a std::map<string, int>, allowing it to efficiently track item frequencies.

The user interacts with the program through a console menu interface with the following options:
Search for an item and display its frequency
Print all item frequencies
Display a histogram representation of item frequencies
Exit the program

The program also creates a backup file (frequency.dat) that stores each item and its count.

The problem this project solves is automating frequency tracking for inventory-style data. Instead of manually counting occurrences, the program reads and processes the file efficiently and presents the results in both numeric and visual (histogram) formats.

What I Did Particularly Well

One area I performed well in was program organization and modular design. I separated functionality into:
main.cpp (user interface and program control flow)
Items.h (class declaration)
Items.cpp (class implementation)

This separation follows good object-oriented programming practices and makes the program easier to understand and maintain.

I also effectively used the C++ Standard Library map container to automatically manage and sort key-value pairs. This simplified frequency tracking and ensured efficient lookups using find().

I implemented:
Proper file handling with error checking (is_open())
Const-correctness in member functions that do not modify the object
Clear and readable output formatting for the histogram feature

Areas for Improvement
There are several ways I could enhance this program:

1. Input Validation
Currently, user input for the menu does not validate non-integer values. Adding stronger validation would prevent runtime errors and improve security.

2. Case Sensitivity Handling
If the input file contains “apple” and the user searches for “Apple,” it will return 0. I could improve this by converting all input to lowercase before storing and searching.

3. File Formatting Improvements
The backup file currently uses the format:
item: quantity
It might be better to store it in a structured format (such as CSV) to allow easier reuse in other applications.

4. Code Efficiency Enhancements
Although std::map is efficient, I could consider using unordered_map if ordering is not required, improving average lookup time from O(log n) to O(1).

These improvements would make the program more efficient, secure, and production-ready.

The most challenging parts of this project were:
Understanding how to properly use std::map
Implementing file input/output correctly
Designing a clean class structure instead of putting everything in main()

I overcame these challenges by:
Reviewing C++ documentation on map
Testing file reading separately before integrating it into the class
Breaking the problem into smaller steps (load file → store data → display results)

I am adding the following to my support network:
C++ reference documentation (cppreference.com)
Stack Overflow discussions on STL containers
Continued practice with modular design and file I/O

Transferable Skills

This project strengthened several skills that are highly transferable:
Object-Oriented Programming (OOP)
File input/output handling
Working with STL containers (map)
Menu-driven program design

Data processing and visualization logic

These skills will apply to future coursework, larger C++ projects, and real-world software development, especially in areas involving data processing or inventory systems.

Maintainability, Readability, and Adaptability

I made the program maintainable and readable by:
Separating class declaration and implementation
Using descriptive function names (printHistogram, getItemQuantity)
Keeping functions focused on one responsibility
Using clear indentation and formatting
Implementing const-correctness where appropriate

The design is adaptable because:
The Items class can easily be reused in other programs
Additional features (such as deleting items, updating counts, or loading different file formats) can be added without modifying the core structure
The menu system can be expanded with minimal changes

This project demonstrates my ability to design a functional C++ application that is organized, readable, and built using industry-standard practices.

