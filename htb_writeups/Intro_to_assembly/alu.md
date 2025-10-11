# Arithmetic Logic Unit (ALU)

## Vocabulary

unary - one operand
binary - two operands

## Useful Info

| Instruction | Description | Example |
| ---- | ---- | ---- |
| not | Bitwise not (invert all bits, 0->1, and 1-> 0) | not rax -> NOT 00000001 -> 11111110 |
| and | Bitwise and (if both bits are 1 -> 1, if bits are different -> 0) | and rax, rbx -> 00000001 and 00000010 -> 00000000 |
| or | Bitwise OR (if either bit is 1 -> 1, if both are 0 -> 0) | or rax, rbx -> 00000001 or 00000010 -> 00000011 |
| xor | Bitwise XOR (if bits are the same -> 0, if bits are different -> 1) | xor rax, rbx -> 00000001 XOR 00000010 -> 00000011 |

## End of chapter challenge

add an instruction to XOR rbx with 15, what is the hex value of rbx after the program has run?

![Screenshot of Challenge Steps](https://github.com/jmcshannon/jmcshannon/images/alu_challenge.png)
