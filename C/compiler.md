# Compiler

To compile a C file run gcc on it

    gcc file.c

This will create an output file called a.out

To show all warnings in the compiler use -Wall 

    gcc file.c -Wall

To actually show all warnings -Wextra and -pedantic should also be used

    gcc file.c -Wextra -pedantic

You can also change the standard of C, for example C99 which doesn't require a return in void functions

	gcc file.c -std=c99

These can also be used in conjunction

# Output file

To change the output file from a.out specify the name with the output flag

    gcc file.c -o outputName


# Single file compilation

The compiler compiles one file at a time, generating an .obj file for each.

# Linker

To create a usable executable the .obj files need to be linked together. After compilation the linker will link these files together for use.



