# Assembly-Loop-Multiply
Multiply two numbers using repeated addition and a loop in Assembly with a picture of the Ram after Run
# Code Breakdown :
```
ORG 001          ; Program starts at memory location 001

LDA Y            ; Load the value of Y into the accumulator
CMA              ; Complement the accumulator (bitwise NOT)
INC              ; Increment the accumulator (effectively: -Y in two's complement)
STA NEGATIVE     ; Store this negative value in variable NEGATIVE

LOOP, LDA PROD   ; Load the current product value
ADD X            ; Add X to the accumulator
STA PROD         ; Store the updated product value back to PROD
ISZ NEGATIVE     ; Increment NEGATIVE and skip next instruction if zero
BUN LOOP         ; Unconditionally branch to LOOP
HLT              ; Halt the program

X, DEC 5         ; Variable X initialized to 5
Y, DEC 4         ; Variable Y initialized to 4
NEGATIVE, DEC 0  ; Variable to store negative of Y (used as loop counter)
PROD, DEC 0      ; Variable to store the product result

END              ; End of program
```
Here's the Ram after Run:![image](https://github.com/user-attachments/assets/4b80f57d-027c-4796-a3f8-5347e807b69e)
