# Intro to ASM - Using the stack

## Vocabulary
stack - segment of memory allocated to the program
LIFO - Last in first out
rsp - Top stack pointer (sp)
rbp - Base stack pointer (bp)
push - add data to top of stack
pop - take data off top of stack

## Useful Info
Because of the LIFO structure you need to push and pop in reverse,
this is covered above, but was worthy of additional scrutiny.

## End of chapter question 
Debug the attached binary to find the flag being pushed to the stack

## Proof

![Screenshot of Challenge Steps](https://github.com/jmcshannon/jmcshannon/blob/main/htb_writeups/images/stack_challenge.PNG)