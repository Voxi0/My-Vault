---
share: true
---
**Tags:** #osdev #programming
OS development is the great pinnacle of programming and teaches you a lot about how computers work as making an operating system means you have to write the code to describe how things are done e.g. how memory is managed.

A very popular and well-known online resource that practically **every** OS developer has come across is [OSDev Wiki](Https://wiki.osdev.org/). It's an extensive collection of resources to aid you in OS development. For example, it has notes that describes what a GDT (Global Descriptor Table) is and how it works etc. It doesn't have all the details and is missing a lot of information but it's still extremely handy.

A thing you must keep in mind with OS development is the fact that you have to do a lot of reading for many things. Like reading the specs sheet for the 8259 PIC (Programmable Interrupt Controller). So be prepared for tons of boring, technical reading if you really want to commit to OSDevving.

You can use more or less any programming language you desire if you have the right tooling but it's recommended for beginners to use C/C++ as most OSDev tutorials and documentation uses it. If you're experienced enough then you can use any language and figure out how to set up the development environment and translate code from C/C++ to something equivalent in your programming language of choice. I'm definitely going with Zig as it has a really neat build system and is literally just C with tons of really cool and modern features.

**ANYWAYS**, getting back to the topic at hand, let's talk about what operating systems are and some other basic concepts of an operating system.
## What's an OS?
An operating system is a piece of software that controls the operations of a computer and manages it's resources.