Header files which ends with `.h` stores function declarations, type definitions and macros that acts as an interface so other source files can use them without duplicating code.

They can be used in a source file using the `#include` [[preprocessor directive]]. This brings these declarations to your source file before it's compiled to machine code instructions. This allows the compiler to understand how to use functions and such defined elsewhere which separates the interface from implementation for cleaner and more organized projects.

