C isn't compiled directly to machine code. There's multiple steps involved in converting C code to machine code that can be executed.
## Summary
- **Preprocessing**: Expands macros and includes while purging all comments outputting a `.i` file containing the cleaned up code that's ready for the actual compilation process.
- **Compiling**: Transforms preprocessed code into assembly code outputting a `.s` file containing all low-level Assembly instructions.
- **Assembling**: Converts assembly code into machine code outputting a `.o` object file.
- **Linking**: Combines object files and resolves function calls into an executable. Outputs the final executable.
## Pre-Processing
Cleans up the code before compiling. It primarily does the following things -
- **Removing Comments:** All single-line and multi-line comments are stripped out of the source code.
- **Macro Expansion:** Any macros e.g. `#define` are replaced by either their values or code snippets.
- **File Inclusion:** `#include` directives are processed by embedding the contents of the included [[Header Files]] into the source code. Recursive inclusions are taken care of as well when included files include other files as well.
- **Conditional Compilation:** The preprocessor also handles conditional compilation directives e.g. `#if`, `#ifdef` and `#endif` to determine which parts of the code to include.
The output is an `.i` file containing the cleaned up, preprocessed code which is now prepared for actual compilation.
## Compiling
In this phase, all preprocessed files `.i` is transformed into low-level Assembly instructions specifically tailored for the target system/CPU architecture. Some of the key things done in this phase are -
- **Lexical Analysis:** The compiler breaks down the code into tokens; keywords, identifiers, operators etc.
- **Syntax Analysis:** The tokens are checked for grammatical structure and transformed into a syntax tree. Basically this stage checks for syntax errors like forgetting to put semicolons at the end of an expression.
- **Semantic Analysis:** The compiler ensures that the code follows the rules of the language e.g. type checks.
- **Optimizations:** Depending on the [[Compiler Flags]], this phase applies various optimizations to improve performance or reduce file size e.g. loop unrolling or constant folding.
The output is a `.s` file containing all the low-level Assembly instructions for the program.
## Assembling
The `.s` Assembly file is now passed to the Assembler which finally converts the Assembly code into machine code (Binary instructions). The output is an object file (`.o`). This is the machine-readable version of the program. Key parts of this phase are -
- **Instruction Translation:** The assembler takes the low-level Assembly instructions e.g. `mov` and converts them to machine instructions.
- **Symbol Resolution:** The assembler resolves labels and references to functions ensuring everything is being addressed properly.
The output is a `.o` object file containing all the machine code for a source file. However, it's not executable just yet.
## Linking
Now, all `.o` object files are combined together into one executable. The linker resolves any external references and prepares the final machine code for execution. Linker flags allows more fine grained control over how object files and libraries are linked together.

There are two types of linking -
- **Static:** All libraries and functions are copied into the executable at compile time making the executable larger in size since all code is embedded. This way, there are no dependencies on external libraries at runtime. Static library files are typically `.a` on UNIX-like systems and `.lib` files on Windows.
- **Dynamic:** Only the references to shared libraries are embedded in the executable. Shared libraries are linked at runtime, making the executable smaller. This way, programs can share common libraries, reducing memory usage and allowing easier updates to libraries without recompiling the entire program. However this way, obviously there are dependencies on external libraries at runtime. Dynamic library files are typically `.so` on Linux or `.dll` on Windows.

Key things done in this phase are -
- **Symbol Resolution:** The linker connects function calls in your code with the correct function definitions, which may reside in other object files or libraries. 
- **Relocation:** The linker adjusts the addresses of variables and functions, ensuring that all addresses are correct once the object files are combined.
- **Adding Startup Code:** The linker adds necessary boilerplate code to set up the environment, such as passing command-line arguments, setting up the stack, and calling the main function. Without this code, the program cannot run properly.