Kevin Qi
108316667

My Var class's eval method first looks for its name in local variable array, if found, 
return that value. If not, then look in global variable array. If not found in either, raise 
EvalError.

My Assign class's exec has two conditions. 1.global 2. not global
If global, then check if the left side is instance of Var or Index. If Var then
add it to our global array variables. If Index, then check if array's name is in our global
variable array and that the position we're indexing is not out of bounds. If satisfied, add
to global array, else raise EvalError.
Now if Assign is not global, check if left side is instance of Var or Index.
If Var, then add it to our local variable array. 
If Index, then check if that array name is in our local variable array and that the index is 
not out of bounds. If not satisfied, raise EvalError. If not found in our local variable array, 
look in global array. If still not found then raise eval error because user is trying to access
an element in an array that doesn't exist.

My Block class goes through all the statements in its block and calls exec on all of them.

For my While and If class, I eval the expression, and call exec on the body if true.

Call class: I create my own localVar array to store local variables within the function. 
I make sure the function called has been defined somewhere in the code. I also make sure that
the arguments passed in are the correct numbers. I add the arguments to my local variable array for
the function and call execute on the body of the function which I have already stored when I looked over
the program in the first sweep.