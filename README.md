# 0x19. C - Stacks, Queues - LIFO, FIFO

## Description
This is a group project in C that focuses on implementing stacks and queues, and understanding the concepts of LIFO (Last-In-First-Out) and FIFO (First-In-First-Out). The project will be done in teams of two people: Adnane Bensouda and Sassi Hamdi Hamdi.

## Project Details
- Project Start: June 20, 2023, 4:00 AM
- Project End: June 23, 2023, 4:00 AM
- Checker Release: June 20, 2023, 10:00 PM
- Auto review will be launched at the deadline.

## Resources
- Google
- How do I use extern to share variables between source files in C?
- Stacks and Queues in C
- Stack operations
- Queue operations

## Learning Objectives
By the end of this project, you are expected to be able to explain the following concepts without the help of Google:
- What do LIFO and FIFO mean
- What is a stack and when to use it
- What is a queue and when to use it
- What are the common implementations of stacks and queues
- What are the most common use cases of stacks and queues
- What is the proper way to use global variables

## Requirements
### General
- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc with the options -Wall -Werror -Wextra -pedantic -std=c89
- All your files should end with a new line
- A README.md file at the root of the project folder is mandatory
- Your code should use the Betty style and will be checked using betty-style.pl and betty-doc.pl
- You are allowed to use a maximum of one global variable
- No more than 5 functions per file
- You are allowed to use the C standard library
- The prototypes of all your functions should be included in your header file called monty.h
- Don't forget to push your header file
- All your header files should be include guarded
- You are expected to do the tasks in the order shown in the project

### GitHub
- There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.

### Compilation & Output
- Your code will be compiled this way: `$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty`
- Any output must be printed on stdout
- Any error message must be printed on stderr

## The Monty Language
Monty 0.98 is a scripting language that is first compiled into Monty byte codes (similar to Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

## Monty Byte Code Files
Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard, but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument.

Example:
push 0
push 1
push 2
push 3
pall
push 4
push 5
push 6
pall


## The Monty Program
Usage: `monty file`

- `file` is the path to the file containing Monty byte code
- If the user does not provide any file or provides more than one argument to your program, print the error message `USAGE: monty file`, followed by a new line, and exit with the status `EXIT_FAILURE`
- If, for any reason, it's not possible to open the file, print the error message `Error: Can't open file <file>`, followed by a new line, and exit with the status `EXIT_FAILURE`
- If the file contains an invalid instruction, print the error message `L<line_number>: unknown instruction <opcode>`, followed by a new line, and exit with the status `EXIT_FAILURE`
- Line numbers always start at 1
- The Monty program runs the bytecodes line by line and stops if either:
    - It executes properly every line of the file
    - It finds an error in the file
    - An error occurs
- If you can't malloc anymore, print the error message `Error: malloc failed`, followed by a new line, and exit with the status `EXIT_FAILURE`
- You have to use malloc and free and are not allowed to use any other function from `man malloc` (realloc, calloc, etc.)

## Quiz Questions
You've completed the quiz successfully! Keep going!

## Tasks
### 0. push, pall
Implement the push and pall opcodes.

#### The push opcode
- The opcode `push` pushes an element to the stack.
- Usage: `push <int>` (where `<int>` is an integer)
- If `<int>` is not an integer or if there is no argument given to push, print the error message `L<line_number>: usage: push integer`, followed by a new line, and exit with the status `EXIT_FAILURE`

#### The pall opcode
- The opcode `pall` prints all the values on the stack, starting from the top of the stack.
- Usage: `pall`
- Format: see example
- If the stack is empty, don't print anything

### 1. pint
Implement the pint opcode.

#### The pint opcode
- The opcode `pint` prints the value at the top of the stack, followed by a new line.
- Usage: `pint`
- If the stack is empty, print the error message `L<line_number>: can't pint, stack empty`, followed by a new line, and exit with the status `EXIT_FAILURE`

### 2. pop
Implement the pop opcode.

#### The pop opcode
- The opcode `pop` removes the top element of the stack.
- Usage: `pop`
- If the stack is empty, print the error message `L<line_number>: can't pop an empty stack`, followed by a new line, and exit with the status `EXIT_FAILURE`

### 3. swap
Implement the swap opcode.

#### The swap opcode
- The opcode `swap` swaps the top two elements of the stack.
- Usage: `swap`
- If the stack contains less than two elements, print the error message `L<line_number>: can't swap, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`

### 4. add
Implement the add opcode.

#### The add opcode
- The opcode `add` adds the top two elements of the stack.
- Usage: `add`
- If the stack contains less than two elements, print the error message `L<line_number>: can't add, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
- The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
    - The top element of the stack contains the result
    - The stack is one element shorter

### 5. nop
Implement the nop opcode.

#### The nop opcode
- The opcode `nop` doesn't do anything.
- Usage: `nop`

## Repository
GitHub repository: [sassi hamdi](https://github.com/sassihamdi-CD/monty)

