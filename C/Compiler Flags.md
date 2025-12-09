These flags changes how code is processed by the preprocessor, compiler and linker. They affect how the final binary turns out by setting optimization levels, enabling/disabling warnings, including/excluding debugging symbols etc. These can be used to either improve performance or customize the behavior. They can be combined together however you desire and the most common ones are listed below.
### General Flags
These flags are extremely common and you'll almost always see them around.
- `-std=<C standard>` - This is used for setting the C standard version to use. As of now, the latest C standard is `c23` and we can set it as so, `-std=c23`.
- `-pedantic` or `-Wpedantic` - Enforces strict ISO C compliance and warns about compiler extensions.
- `-Wall` - Enables a large set of useful compiler warnings to be detected and reported to the programmer.
- `-Werror` - Turns all warnings into compilation errors, stopping the [[Compilation Process]] if any warnings are encountered.
- `-Wextra` or just `-w` - Enables extra compiler warnings that aren't enabled by `-Wall`.
- `-g` - Adds debugging symbols to executable which makes it easier to use a debugger. It increases the file size though.
- `-o` - To set the filename of the output file.
### Optimizing
- `-O0` - No optimizations for faster builds making it suitable for debug builds.
- `-O1` - Just basic optimizations used for release builds. It's not as commonly used as `-O2` though.
- `-O2` and `-O3` - Higher levels of optimization which increases build time but  increases performance. However, `-O3` is aggressive which can make the executable larger and sometimes even slower. `-O2` is commonly used for release builds.
- `-OFast` - An even higher level of optimization than `-O3`. This enables a lot of flags as well.
- `-DNDEBUG` - Removes all `assert()` checks by defining the `NDEBUG` [[Macros]] which can make the executable slightly faster. Used for release builds.
- `-s` - Strips the executable of anything that isn't required to run the program e.g. debug info and symbol tables which leads to a huge reduction in file size. Used for release builds.