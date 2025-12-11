Header files which ends with `.h` stores function declarations, type definitions and macros that acts as an interface so other source files can use them without duplicating code.

They can be used in a source file using the `#include` [[Preprocessor Directives]]. This brings these declarations to your source file before it's compiled to machine code instructions. This allows the compiler to understand how to use functions and such defined elsewhere which separates the interface from implementation for cleaner and more organized projects.

These files always begins with either `#pragma once` or something slightly longer -
```c
#ifndef <whatever name you want>_H
#define <whatever name you want>_H

#endif
```

These are known as header guards. Both of these header guards does the exact same thing which is ensuring that even if the header file is included by multiple other files, everything declared inside the header file won't be repeated again because if it was then the compiler would throw a bunch of redefinition errors at us of course.

You can use either guard but I always tend to reach out for `#pragma once` since it's much shorter and nicer in my opinion.

Typically you'd replace `<whatever name you want>` with the name of the header file itself followed by a `_H` but you can name the define whatever you want. Just make sure that you don't use the same name in any other header file.