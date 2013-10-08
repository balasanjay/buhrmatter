buhrmatter
==========

A clang-format utility.

It will automatically format your C++ closer to the slightly-quirky format laid out
[here](https://www.student.cs.uwaterloo.ca/~cs343/C++CodingGuidelines.shtml).

Note that the tool does not have perfect coverage; some amount of work is still necessary
to make your code fully adhere to the style guide.

Disclaimer
---------

`clang-format` rewrites your source-code. Make sure to have your code in a source-control system, 
so it can't do any permanent damage.

Instructions
-------------

     $ cd <my-project>
     $ curl "https://raw.github.com/balasanjay/buhrmatter/master/format-style" > .clang-format
     $ clang-format -i *.h *.cc

Note that `clang-format` is idempotent, so you can run it as many times as you want.

Requirements
------------

In order to use this tool, you need two things.
+ `clang-format`
+ A style-file (this is provided by this repo; see the `curl` command above)

There are two ways to get `clang-format`; you can build from source, or just use the provided binaries. 
Note that building from source can take a considerable amount of time.

Building clang-format from source
---------------------------------

    $ cd ~
    $ svn co http://llvm.org/svn/llvm-project/llvm/trunk llvm
    $ cd llvm/tools
    $ svn co http://llvm.org/svn/llvm-project/cfe/trunk clang
    $ cd ~/llvm
    $ ./configure
    $ make

After executing the instructions above, `clang-format` will be in `~/llvm/Debug+Asserts/bin/clang-format`.

Using the provided binaries
---------------------------
[For OSX](https://github.com/balasanjay/buhrmatter/releases)

[For Linux](https://dl.dropboxusercontent.com/u/2795539/clang-format) (thanks, Kalsi!)

