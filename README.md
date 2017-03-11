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

llvm-binutils is licensed under the same terms as the Varuna compiler. See the file LICENSE for details.

Copyright (C) 2016-2017 Elias Kosunen

llvm-binutils mainly contains mirrored code from the LLVM compiler infrastructure project.
See the whole license at http://releases.llvm.org/3.9.1/LICENSE.TXT

University of Illinois/NCSA
Open Source License

Copyright (c) 2003-2016 University of Illinois at Urbana-Champaign.
All rights reserved.
