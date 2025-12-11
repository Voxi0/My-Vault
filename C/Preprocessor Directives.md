These are special instructions in your C code used by the preprocessor before actual compilation. These always start with a `#` followed by the action the preprocessor should perform e.g. `#include` to include the contents of a specified file, typically [[Header Files]]. These directives always end at the end of the line unless a backslash (`\`) is used to continue it to the next line.

The most common directives that you'll see and should know are listed below.
- [[Macros]]
- `#include` - Brings in the content of a header file by pretty much copy-pasting. There's two types of includes, `#include` with `<>` is used to include a header file that's located inside of an include directory that the compiler will search while a `#include` followed by `""` are relative includes to include a header file from the current directory. You'll typically lean towards the `<>` but relative includes are sometimes used as well albeit not as often.
- `#ifdef` and `ifndef` - For conditional compilation which means compiling parts of code only if a [[Macros]] is defined or not defined. This is incredibly powerful and is usually used for allowing programmers to easily include/exclude extra code for debugging their program.
- `#if` / `#elif` / `#else` / `#endif` - Conditional compilation based on expressions. I think this is pretty self-explanatory and obviously again, these allows you to compile parts of code only if certain conditions evaluates to true.
- `#pragma` - Provides compiler-specific instructions.
- `#error` - Triggers a compilation error with a message.