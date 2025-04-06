**Tags:** #zig #programming
## Intro
Zig is a general purpose programming language and toolchain for maintaining robust, optimal, and reusable software.
- **Robust** - Behaviour is correct, even for edge cases such as out of memory.
- **Optimal** - Write programs the best way they can behave and perform.
- **Reusable** - The same code works in many environments which have different constraints.
- **Maintainable** - Precisely communicate intent to the compiler and other programmers. The language imposes a low overhead to reading code and is resilient to changing requirements and environments.
## Features
- A small and simple making it very beginner friendly.
- Cross-compilation is a first class feature of Zig.
- No hidden control flow, memory allocations, no preprocessor and macros. All control flow is managed exclusively with language keywords and function calls. Makes Zig code very readable and predictable.
- Memory is manually managed and memory allocation failures must be handled by the programmer. Any functions that must allocate memory accept an allocator parameter. As a result, the Zig Standard Library can be used even for the freestanding target. Zig provides `defer` and `errdefer` to make all resource management - not only memory - simple and easily verifiable.
- Integration with C libraries without FFI/bindings. `@cImport` directly imports types, variables, functions, and simple macros for use in Zig. It even translates inline functions from C into Zig. Zig is also a C compiler!
- A fresh take on error handling as errors and values and cannot be ignored, they must be handled with `catch`.
- Compile-time reflection and code execution. Functions and blocks of code can be evaluated at compile time. Zig evaluates as many things as possible at compile time internally as well to improve performance.
- 4 build modes allowing you choose between both safety and performance. Zig also claims to be more performant than C.
- Zig aims to compete with C so the Zig standard library only integrates with LibC but doesn't depend on it.
- Top level declarations e.g. global variables are order independent and lazily analyzed and are evaluated at compile time. So they can be placed and used anywhere in a Zig file.