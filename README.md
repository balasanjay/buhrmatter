buhrmatter
==========

A clang-format utility.

It will automatically format your C++ closer to the slightly-quirky format laid out here:
[here](https://www.student.cs.uwaterloo.ca/~cs343/C++CodingGuidelines.shtml).

Note that the tool does not have perfect coverage; some amount of work is still necessary
to make your code fully adhere to the style guide.

Building clang-format from source
==

    $ cd ~
    $ svn co http://llvm.org/svn/llvm-project/llvm/trunk llvm
    $ cd llvm/tools
    $ svn co http://llvm.org/svn/llvm-project/cfe/trunk clang
    $ cd ~/llvm
    $ ./configure
    $ make

After executing the instructions above, `clang-format` will be in `~/llvm/Debug+Asserts/bin/clang-format`.
