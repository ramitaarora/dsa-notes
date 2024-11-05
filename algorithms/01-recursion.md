# Recursion

### Recursion
- Calling the function within the function
- A strategy for solving problems by defining the problem in terms of itself
- Programmers use recursion when they need to perform a similar action multiple times in a row until it reaches a predefined stopping point, also known as a base case.
- When analyzing the Big O runtime of recursive functions, we count the relation of input to function calls.

### A recursive approach requires the function invoking itself with different arguments
- Languages make this possible with <i>call stacks</i> and <i>execution contexts</i>
    - <b>Stacks</b>, a data structure, follow a strict protocol for the order data enters and exits the structure: <i>the last thing to enter is the first thing to leave.</i>
        - Your programming language often manages the call stack, which exists outside of any specific function. 
        - This call stack tracks the ordering of the different function invocations, so the last function to enter the call stack is the first function to exit the call stack.
    - An <b>execution context</b> contains the variables within each recursive call.


### Recursion has two fundamental aspects: <i>the base case</i> and the <i>recursive step.</i>

- When using iteration, we rely on a <i>counting variable</i> and a <i>boolean condition</i>
    - For example, when iterating through the values in a list, we would increment the counting variable until it exceeded the length of the dataset.
- <b>Base case</b> – the conditions under which the function returns a value without making any additional calls to itself.
    - The base case dictates whether the function will recurse, or call itself. Without a base case it’s the iterative equivalent to writing an infinite loop.
    - There is no recursive call in a base case.
    - The "else"
- <b>Recursive case</b> – the conditions under which the function will perform an action and call itself.
    - The recursive step moves us closer to the base case. 
    - In an iterative function, this is handled by a loop construct that decrements or increments the counting variable which moves the counter closer to a boolean condition, terminating the loop.
    - In a recursive function, the “counting variable” equivalent is the argument to the recursive call.
    - A recursive function which has no base case, or a recursive step that does not lead to the base case, will cause a <i>stack overflow</i>.
    - The "if" / "else if"

