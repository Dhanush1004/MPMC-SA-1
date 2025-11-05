# MPMC-SA-1

# 7.Write an assembly language program in 8086 to find the factorial of a given number and store the result in memory

# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

## APPARATUS REQUIRED
- Personal computer with Keil software

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END
```
## OUTPUT

<img width="533" height="466" alt="image" src="https://github.com/user-attachments/assets/318e1660-a817-4731-9c0c-a346f21b8a32" />
<img width="696" height="392" alt="image" src="https://github.com/user-attachments/assets/fa5ca29f-a208-44b5-ad75-7dbd5e6891b7" />


## MANUAL CALCULATIONS
<img width="671" height="309" alt="image" src="https://github.com/user-attachments/assets/d904bddf-5450-4305-af9c-9032412399af" />

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.


