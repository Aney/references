# Preprocessor

The preprocessor comes before the compiler. 

It's job is to prepare the source code for compilation.

Anything that begins with a `#` is for the preprocessor, such as includes

    #include <stdio.h>

    #include "multiply.h"

Which tells the compiler to compile these files together as one

The preprocessor can also be used for macros

    #define SQUARE(x) multiply(x,x)

Macros, when called aren't like typical functions, instead the preprocessor replaces the macro call with the code itself.

`SQUARE(10)` would be replaced with `multiply(10,10)`

They can generate allsorts of code, such as CONSTANTS

    #if LEVEL > 0
    	/* conditionally do this code */
    #endif
