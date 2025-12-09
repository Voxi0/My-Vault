These are options passed to just the linker to control it's behavior. These flags are typically used for specifying which libraries to link the executable against and define various other settings related to the linking process. There are a bunch of linker flags to mess with though not as much as [[Compiler Flags]]. Though, you'll almost never need to use any more flags than the ones listed below unless you dive into operating systems development or some other low-level shenanigans.
### General
- `-L` - Tells the linker which directories to search for libraries.
- `-l` - Links the executable against a specified library.
- `-shared` - To create a shared library instead of an executable.
- `-static` - To link against static libraries instead of shared libraries.
- `-o` - To set the filename of the output file.