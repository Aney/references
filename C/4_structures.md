# Structures

A collection of variables that create a new type, like classes/objects, but pure data.

Keep related variables and values together.

    typedef struct Pixel{
    	float X;
    	float Y;
    }

Declared as any other variable type

    Pixel p;

With initialisation

	Pixel p = {10.0f, 25.0f};

If typedef not before the original struct, it'll need to be added. Structs are in a different namespace.

	struct Pixel p;

You can assign and access members of the declared structs using a .

    float x_value = p.X;

    p.Y = 66.0f;

## Layout and Padding

C and C++ compilers require values in structs to be in order of sizeof, so shorts before ints, etc.
If this isn't the case the struct will take up more memory that needed. eg.

    short x; // 2 bytes, with 2 bytes of padding
    int y; // 4 bytes, no padding 
    short z; // 2 bytes, 2 bytes of padding
	// total 12 bytes

    short x; // 2 bytes
    short z; // 2 bytes 
    int y; // 4 bytes
	// total 8 bytes
