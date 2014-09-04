MustScript Interpreter
=========
This is an interpreter for our simple programming language, MustScript.
It takes as input a single argument, the name of the input file containing a MustScript program. 
Then it tries to parse the input program, execute the program, and print the following outputs:
1. If the input program contains a syntax error, the interpreter prints 'Parsing Error' and exits.
2. Else, if any of the conditions in MustScript are violated, then the interpreter catches the error and 
prints 'Evaluation Error'
3. If no error is found, then the program should execute as specified.
![s1](https://raw.githubusercontent.com/kevinkeyjkw/307hw4/master/ScreenShot1.jpg)
