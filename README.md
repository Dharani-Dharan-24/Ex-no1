# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />

#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="1280" height="726" alt="WhatsApp Image 2026-05-14 at 10 35 28 AM" src="https://github.com/user-attachments/assets/3edd2989-fb81-4807-91c8-a4260e271782" />

#### Manual Calculations

<img width="1280" height="460" alt="WhatsApp Image 2026-05-14 at 10 31 10 AM" src="https://github.com/user-attachments/assets/494bc678-bffd-4c34-9138-fde9a5e5fd10" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="1111" height="753" alt="WhatsApp Image 2026-05-14 at 10 37 04 AM" src="https://github.com/user-attachments/assets/15d9cc43-cd5a-4875-a3c4-e6045bbb58ad" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />

#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```
#### Output Table

<img width="781" height="422" alt="2 - ot" src="https://github.com/user-attachments/assets/2715a90e-059d-4a38-a392-71132c4c5d02" />

#### Manual Calculations

<img width="826" height="227" alt="2 mc" src="https://github.com/user-attachments/assets/fba3d74c-d6f6-4029-b0a2-849963b06109" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="782" height="421" alt="2 out" src="https://github.com/user-attachments/assets/f3d36eff-e11b-48f9-aa23-0280689b1bef" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />

#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="754" height="415" alt="3 ot" src="https://github.com/user-attachments/assets/5d4d84af-ee73-493d-a8b7-b5d21197c663" />

#### Manual Calculations

<img width="734" height="314" alt="3 mc" src="https://github.com/user-attachments/assets/c354e1b3-4e17-4c1d-95eb-f931a5f6a00f" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="837" height="433" alt="3 out" src="https://github.com/user-attachments/assets/2f8dcd2e-e716-48a5-852c-16d0763a091b" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />

#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```
#### Output Table

<img width="758" height="418" alt="4 ot" src="https://github.com/user-attachments/assets/bf9cc4f1-4893-4de4-81b1-72ac438c60a3" />

#### Manual Calculations

<img width="772" height="296" alt="4 mc" src="https://github.com/user-attachments/assets/db0a517f-25cb-4e64-b3cd-ffabc768796b" />

---
## OUTPUT FROM MASM SOFTWARE
<img width="818" height="445" alt="4 out" src="https://github.com/user-attachments/assets/1b5ceead-51c4-4b6a-8c7a-25f52202ae7e" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

