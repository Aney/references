# Loops

Loops, or iteration statements are executed repeatedly until their iteration has completed.

## While

While loops check a condition and execute the statement inside the loop if the condition is evaluated as true.

    while (condition) { 
    	statement;
    } 

To ensure you don't get infinite loops, the evaluation must eventually become false.

    while (count < 10) {
	    printf("%d \n", count);
    	count += 1;
    }

## Do

Do loops, or Do while loops also execute the statement inside the loop. 

Unlike the while loop the Do loop will always execute the statment at least once, as it does the evaluation of the condition after the statements.

    do {
	    printf("%d \n", count);
    	count += 1;
    } while (count < 10);

This is useful in case the statement must be run, but could also be iterated after this first execution. Like a normal statement followed by a while loop, but cleaner and more efficient.

## For

Iterates through in a single condition. 

Defines the varialbe, sets the condition, and also the increment that should happen if the condition is met.

    for (int count = 10; count < 10; count +=1) {
    	statement;
    }

## Break and Continue

Break can break out of statements, and loops

Continue skips over the code, and returns to the loop continuing from the next value.
