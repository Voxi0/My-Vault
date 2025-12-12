The C standard library is a specification defined by the ISO C standard which details all the basic functions that all C programs should have access to. The libc on the otherhand is an implementation of the standard library e.g. musl, glibc, mlibc etc.

This standard provides a portable API allowing programmers to do many things e.g. I/O handling, memory management, math operations etc. Think of it as an abstraction layer over platform-specific things while also providing general-purpose utilities.

Because the API is standardized, the programmer doesn't need to worry about how the underlying operating system works. This means that programs using the standard library and not relying on anything OS-specific would compile on other operating systems with little to no changes to the code making the code very portable.

This greatly simplifies programming and saves a lot of time since the programmer doesn't have to understand and directly interact with the operating system which would've made the code more complex and harder to write and far less portable.
## Non-Standard Extensions
Most implementations of the C standard library actually offers additional functionality that isn't part of the ISO C standard. These are called non-standard extensions. While they may be convenient and useful, it's bad to rely on them too much because they reduce portability. Code using these extensions may not compile on another system or another libc unless they support all the extensions that the program needs.
- Because operating systems have features that weren't covered by the ISO C standard
- Vendors want convenient functions