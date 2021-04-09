**MINI-ASSIGNMENT#1**

**COMPILERS AND THEIR OPTIONS**

K. LAKSHMI SRAVYA

CS19BTECH11017

**VARIOUS OPTIONS IN COMMON COMPILERS: GCC AND LLVM**

There are many options in GCC like

- -o to specify the output executable name (gcc main.c -o main),
- -Wall to enable all warnings set,
- producing only
 -- preprocessor output with -E option,
 -- assembly code using -S option,
 -- compiled code using -C option,
- producing all intermediate files using -save-temps function,
- -l to link with shared libraries,
- -V to print all the executed commands,
- -D to use compile time macros,
- -Werror to convert warnings into errors,
- providing gcc options through a file using @ option.

List of all the available options in GCC can be referred from the following link
[https://gcc.gnu.org/onlinedocs/gcc/Option-Summary.html](https://gcc.gnu.org/onlinedocs/gcc/Option-Summary.html)

There are different types of options in LLVM

1) Stage Selection Options like
- -E to run the preprocessor stage,
- -S to run the previous stages as well as LLVM generation and optimization stages and target-specific code generation, producing an assembly file.

2) Language Selection and Mode Options like
- -x <language> to treat subsequent input files as having type language,
- -std=<standard> to specify the language standard to compile for,
- -trigraphs to enable trigraphs,
- -fms-extensions to enable support for Microsoft extensions.

3) Target Selection Options like
- -arch <architecture> to specify the architecture to build for,
- -mcpu=?, -mtume=? as an alias for -print-supported-cups.

4) Code Generation Options like
- -O0, -O1, -O2, -O3, -Ofast, -Os, -Oz, -Og, -O, -O4 to specify the optimization level to use.
- -g to Generate debug information.
- -fvisibility to set flag to the default visibility level.

5) Driver Options like
- -### to print (but do not run) the commands to run for this compilation.
- -print-file-name=<file> to print the full library path of file.
- -v to show commands to run and use verbose output.

6) Diagnostics Options like -fshow-column, -fshow-source-location, -fcaret-diagnostics, -fdiagnostics-fixit-info, -fmessage-length. These options control how Clang prints out information about diagnostics (errors and warnings).

7) Preprocessor Options like
- -D<macroname>=<value> to add an implicit #define into the predefines buffer which is read before the source file is preprocessed.
- -U<macroname> to add an implicit #undef into the predefines buffer which is read before the source file is preprocessed.
- -I<directory> to add the specified directory to the search path for include files.

List of all the available options in LLVM Clang can be referred from the following link
[https://clang.llvm.org/docs/CommandGuide/clang.html](https://clang.llvm.org/docs/CommandGuide/clang.html)

**VARIOUS FRONTENDS THAT THESE COMPILERS SUPPORT**

Frontends that GCC support

- GNU Pascal Compiler (GPC)
- Mercury
- Cobol for GCC
- GNU Modula-2
- GNU Modula-3
- GHDL (Frontend of VHDL)
- PL/1 for GCC (Frontend for PL/I language)
- GCC Unified Parallel C (GCC UPC)

Frontends that LLVM support

- Clang (C language family includes C, C++, Objective C/C++, OpenCL, CUDA, Render Script).

**USE THESE COMPILERS TO GENERATE CODE FOR VARIOUS ARCHITECTURES USING ITS VARIOUS BACKENDS AND REPORT YOUR FINDINGS.**

Given a file compiler.c
gcc compiler.c -S produces architecture file of compiler.c produced by GCC
clang compiler.c -S produces architecture file of compiler.c produced by LLVM
Output of the above two commands would be different as the compilers are different.

**COMPILERS COME WITH VARIOUS OPTIMIZATION LEVELS: FOCUSING ON OPTIONS O0, O1, O2, O3 AS WELL AS -OS, -OZ..**

Given options are used to specify the optimization level 

- -O0 => no optimization (this level compiles the fastest and generates the most debuggable code).
- -O1 => somewhere between -O0 and -O2.
- -O2 => moderate level of optimization which enables most optimizations.
- -O3 is like -O2, except that it enables optimizations that take longer to perform or that may generate larger code (in an attempt to make the program run faster).
- -Ofast enables all the optimizations from -O3 along with other aggressive optimizations that may violate strict compliance with language standards.
- -Os is like -O2 with extra optimizations to reduce code size.
- -Oz is like -Os(i.e, -O2), but reduces code size further.
- -Og is like -O1.In future, this option would disable different optimizations in order to improve debuggability (development in progress).
- -O is equivalent to -O1.
- -O4 and higher are equivalent to -O3.
