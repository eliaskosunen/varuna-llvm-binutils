# llvm-binutils

LLVM binary utilities for the Varuna compiler.
These are provided with the compiler so clients don't have to install LLVM to compile Varuna programs

## Installing

This repository is meant to be used as a `git submodule` for the Varuna compiler,
in the directory projects/llvm-binutils.

```sh
# In compiler root
$ git submodule add https://github.com/varuna-lang/llvm-binutils.git projects/llvm-binutils
```

## License

Vart is licensed under the same terms as the Varuna compiler. See the file LICENSE for details.

Copyright (C) 2016-2017 Elias Kosunen
