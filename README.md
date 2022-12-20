# Monty

Monty 0.5 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

## Monty byte code files

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:

```
 push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$

```

Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:

```
push 0 Push 0 onto the stack$
push 1 Push 1 onto the stack$
$
push 2$
  push 3$
                   pall    $
$
$
                           $
push 4$
$
    push 5    $
      push    6        $
$
pall This is the end of our program. Monty is awesome!$

```

# Usage:
Clone the repository and run;

```
 gcc -Wall -Werror -Wextra -pedantic *.c -o monty.

```

To execute your program run:

```
 ./monty test/file
```

Available operation codes:

| Opcode | Description                                                                                                                                                                                        |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| push   | Pushes an element to the stack. e.g (push 1 # pushes 1 into the stack)                                                                                                                             |
| pall   | Prints all the values on the stack, starting from the top of the stack.                                                                                                                             |
| pint   | Prints the value at the top of the stack.                                                                                                                                                          |
| pop    | Removes the to element of the stack.                                                                                                                                                               |
| swap   | Swaps the top to elements of the stack.                                                                                                                                                            |
| add    | Adds the top two elements of the stack. The result is then stored in the second node, and the first node is removed.                                                                               |
| nop    | This opcode does not do anything.                                                                                                                                                                  |
| sub    | Subtracts the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed.                                              |
| div    | Divides the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed.                                                |
| mul    | Multiplies the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed.                                             |
| mod    | Computes the remainder of the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed.                              |
| #      | When the first non-space of a line is a # the line will be trated as a comment.                                                                                                                    |
| pchar  | Prints the integer stored in the top of the stack as its ascii value representation.                                                                                                               |
| pstr   | Prints the integers stored in the stack as their ascii value representation. It stops printing when the value is 0, when the stack is over and when the value of the element is a non-ascii value. |
| rotl   | Rotates the top of the stack to the bottom of the stack.                                                                                                                                           |
| rotr   | Rotates the bottom of the stack to the top of the stack.                                                                                                                                           |
| stack  | This is the default behavior. Sets the format of the data into a stack (LIFO).                                                                                                                     |
| queue  | Sets the format of the data into a queue (FIFO).                                                                                                                                                   |

# 0x19. C - Stacks, Queues - LIFO, FIFO
**About:** In this project, we created a simple interpreter for\
 Monty ByteCodes. The interpreter reads a bytecode file and exe\
cutes the bytecode commands.
### The Monty language
Monty 0.98 is a scripting language that is first compiled into \
Monty byte codes (Just like Python). It relies on a unique stac\
k, with specific instructions to manipulate it.

### Monty byte code files
Files containing Monty byte codes usually have the .m extension\
. Most of the industry uses this standard but it is not require\
d by the specification of the language. There is not more than \
one instruction per line. There can be any number of spaces bef\
ore or after the opcode and its argument: [examples](#Examples)

## Objectives:
* To know what LIFO and FIFO mean
* To know what a stack is, and when to use it
* To know what a queue is, and when to use it
* To know the common implementations of stacks and queues
* To know the most common use cases of stacks and queues
* To know the proper way to use global variables


### Resource:
* [Difference between Stack and Queue Data Structures](https://\
www.geeksforgeeks.org/difference-between-stack-and-queue-data-s\
tructures/)
