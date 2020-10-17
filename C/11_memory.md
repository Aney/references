# Memory

    int i = 121313;

Tells the computer to put aside some memory for i, as an integer.

This is stored at a certain memory address.

    %i;
    printf("0x%p\n", &i);

The value will then be stored in that memory and can be referenced with the variable name, or with a pointer.

# Pointers

Pointer's can reference a memory address, this is like a varialbe that stores a memory address;

    int * p = &i;

    int * p = 0;

Pointers set to 0 have no memory address, but should be declared as such instead of with no initialisation, as no init could cause bugs and other issues. 

# Derefferenced Pointers

Pointers can also be dereffernced to get the value being pointed to, istead of the memory address itself.

    int j = *p;

j is a referrence of p's memory address, the actual value of the varialbe it's pointed to.

    *p = 34234;

The derefferenced value of p can be altered, while keeping the same memory address through derefferencing.
