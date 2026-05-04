---
cssclasses:
  - notebook
tags:
  - nix
---
[Nix](https://nixos.org/) is a package manager developed by [Eelco Dolstra](https://edolstra.github.io/) as part of his PhD thesis in 2003. It's aim is to address the shortcomings of traditional imperative package managers. Nix is a declarative package manager which makes it unique since package managers are usually imperative in nature.

Packages installed with Nix are neatly arranged inside of `/nix/store` instead of scattering files around the system. Each package is isolated into it's own directory inside of `/nix/store` with their names containing a cryptographic hash. The folders also contain everything required to build the package including dependencies