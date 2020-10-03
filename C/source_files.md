# Source Files

# Source

Source files need to be declared in the source file it's called in.

- main.c
    int main(){ multiply(4,5); }

- multiply.c
    int multiply(int x, int y){ return x * y; }

Definitions in multiple need to be declared in main to be called.

Function declaration could be added to main.c above the main function, and this would allow for function calls.

However multiply's functions may want to be used in multiple different source files

# Header

Header files are used for declaration so they can be used in other source files.

- multiply.h
    int multiply(int,int);

This header file will then be added to the main.c source file, at the top.

- main.c
    #include "multiply.h"

That will include the contents of the multiply header file to the source file.
