# Unions

Probably won't be used much, eh.

Like a structure, but all members share the same (starting) memory address

    typedef union testUnion{
    	int Int;
    	float Real;
    }

A union is the size of it's biggest member (in bytes)

A union will be one of these types, so either an int or float depending on what it's set as.


This can be useful for APIs, or if a variable could be a number of types. More likely the former. 
