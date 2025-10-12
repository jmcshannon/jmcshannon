# Intro to ASM - Unconditional Branching

## Vocabulary

jmp - jump to a location unconditionally

## Useful Info

jmp without a conditional is similar to a while true loop and
probably shouldn't be used in loops as it doesn't decrement rcx
it just jumps over it, depending on where it is I guess.

## End of chapter question

Try tp jump to "func" before "loop loop", what is the hex value of "rbx" register
at the end.

This essentially short circuits the loop and jumps straight to func
so the rbx register is the same as when the loop was initially started

```Assembly
global _start

section .text
_start:
    mov rbx, 2
    mov rcx, 5
loop:
    imul rbx, rbx
    jmp func
    loop loop
func:
    mov rax, 60
    mov rdi, 0
    syscall
```
![Screenshot of Challenge Steps](https://github.com/jmcshannon/jmcshannon/blob/main/htb_writeups/images/unconditional_challenge.PNG)

