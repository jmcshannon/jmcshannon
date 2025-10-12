# Intro to ASM - Conditional branching

## Vocabulary

| Instruction | Condition | Description |
| ---- | ---- | ---- |
| jz | D = 0 | Destionation equal to zero | 
| jnz | D != 0 | Destination **not** equal to zero |
| js | D < 0 | Destination is negative |
| jns | D >= 0 | Destination is not negative |
| jg | D > S | Destination is greater than source |
| jge | D >= S | Destination is greater than or equal to source |
| jl | D < S | Destination less than source |
| jle | D <= S | Destination less than or equal to source |
| cmp | cmp rax, rbx -> rax - rbx | Sets RFLAGS by subtracting the second operand from the first operand |


## RFLAGS and EFLAGS

High level important bits because there are several flags and I don't want 
to make a table that big

CF = Carry Flag
ZF = Zero Flag
PF = Parity Flag
SF = Sign Flag
Zero flag on means value > 0, Zero flag off means value = 0

32-bit version is EFLAGS, 16-bit version is FLAGS

## Useful info
loop is just a combination of dec rcx and jmp, but more efficient since it is
such a common thing to do, however conditional jump instructions are much
more efficient.

The main benefit of cmp is that is does not affect operands, it just compares them
and does not store the result anywhere.

In a cmp instruction the first operand must be a register, whereas the other can be a
register, variable, or intermediate value

## End of chapter question

The attached asm loops forever, modify rax instruction to make it not loop, what hex value prevents the loop

```Assembly
global _start

section .text
_start:
    mov rax, 2      ; change here
    imul rax, 5
loop:
    cmp rax, 10
    jnz loop
```

![Screenshot of Challenge Steps](https://github.com/jmcshannon/jmcshannon/blob/main/htb_writeups/images/conditional_challenge.PNG)




