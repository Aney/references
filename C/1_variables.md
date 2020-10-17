# Variables

Declare then use variables

<type> <name> (optional initialiser) e.g. `int hens = 5`

Variables should be declared seperately.

If variables aren't initialised it'll try to get some value from the stack, causing massive unprodictibiliy. Always initialse.

## Types

These types store a certain amount of data, in bits.

- int
- float
- double
- char

- unsigned
- short
- long

## Signed and Unsigned

integers are signed by default, allowing negatives and positives.

Unsigned ints, etc. have all their bits for positive values.


## Local Variables

These are only usable and accessible withing the scope of the current function

## Static Varialbles

Static variables retain their value within the function, regardless of how many function calls.

static int hens; 

Static variables default their initialisation to 0. And are not re-initialised upon function calls. These variables retain their value until the program is restarted, etc.

### Sharing static varialbes

By declaring the static variable within the source code, not inside of a function it can be used by many functions.

Global?
