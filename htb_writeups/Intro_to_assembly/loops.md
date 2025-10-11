# Loops in asm

## Vocabulary

Loop - A set of isntructions that repeat for rcx times.

### Useful

Load loop iteration into rcx, ex mov rcx, 5

Define the loop ex:

loop:
    imul rax, rax
    loop loop

Asm doesn't seem to have issues with variable namespaces?

### End of chapter question

Edit the asm to run the loop 5 times, what is the hex value of rax by the end

![Screenshot of Challenge Steps](https://github.com/jmcshannon/jmcshannon/blob/main/htb_writeups/images/loops_challenge.PNG)
