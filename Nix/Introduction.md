---
cssclasses:
  - notebook
tags:
  - nix
---
In 2003, [Eelco Dolstra](https://edolstra.github.io/) created the declarative package manager called Nix as part of his PhD thesis to address the shortcomings of traditional package managers.

It adheres to the declarative programming paradigm therefore the user is expected to edit a file to declare what packages must be installed. Nix combines both the functional programming paradigm and declarative programming paradigm together with all packages being represented as functions. This makes Nix deterministic and amazing for software deployment and such.

Nix isolates each package in a directory whose name is a cryptographic hash. The directory contains all input data e.g. the dependencies for a given package. This way, the dependencies for each and every package is isolated which gets rid of interference since each program can have their own version of the same thing.

All these packages are stored in `/nix/store` so they're all neatly arranged in a single directory rather than having all the files for a package be scattered all throughout the system.