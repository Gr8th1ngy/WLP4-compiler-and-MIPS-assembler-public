# Please contact me at hdanguye@uwaterloo.ca for access to code.

# WLP4 compiler and MIPS assembler
 A compiler for a [subset of C++](https://www.student.cs.uwaterloo.ca/~cs241/wlp4/WLP4tutorial.html) and assembler for a [subset of MIPS](https://www.student.cs.uwaterloo.ca/~cs241/mips/mipsref.pdf)

# Usage:
Let's say the file needed to compile is called `hello_world.wlp4`.

Run the following command: `wlp4scan <hello_world.wlp4 | wlp4parse | wlp4gen >out.mips` where `out.mips` is the output file containing the MIPS assembly language.  
The file `out.mips` can be assembled by `asm <out.mips >binary` where `binary` is the binary executable.

# Breakdown:

`wlp4scan` scans the `wlp4` file and tokenizes this file.  
`wlp4parse` reads the tokenized version and outputs a parse tree, checking for compiler errors.  
`wlp4gen` reads the parse tree and prints out the assembly language file.  
`asm` assembles a MIPS file into a binary executable.
