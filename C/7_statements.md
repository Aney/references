# Conditional Statements

Code that gets executed

# Conditional/Selection Statements

## If Statement

Evaluates a condition and executes different compound statements depending on the evaluation.

    if (!condition) statement;

Ideally you want to wrap the code blocked statements in braces

    if (condition) {
    	statement;
    }
    else{
    	statement2;
    }

You can also add more conditions if the first doesn't match, if the other conditiosn also don't match then the else will execute.

    if (condition) {
    	statment;
    }
    else if (condition2){
    	statement2;
    }

C doesn't have an elseif, elif, etc. Instead it just performs another if statement after the else clause.

## Switch statement

Select from a number of different values/case depending on the switch value

    switch (eggs) {
    	case 0: printf("no eggs"); break;
    	case 1: printf("one egg"); break;
    	default: printf("default value if neither case match switch"); break;
    }

In C if the breaks aren't there, it'll execute code from that match. This includes all the cases after the match.
