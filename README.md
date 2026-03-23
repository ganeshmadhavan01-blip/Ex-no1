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

<img width="566" height="558" alt="image" src="https://github.com/user-attachments/assets/1cb487da-cb94-4d89-9ed5-dcea66a13519" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="643" height="382" alt="image" src="https://github.com/user-attachments/assets/0a1905df-a09d-4110-93f1-b9c42118ee89" />


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

<img width="503" height="212" alt="image" src="https://github.com/user-attachments/assets/ae401351-391f-4823-9356-97644169751b" />


#### Manual Calculations

<img width="329" height="277" alt="image" src="https://github.com/user-attachments/assets/ca2eb321-4ee5-4d2e-b120-b204d07f9506" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="609" height="399" alt="image" src="https://github.com/user-attachments/assets/6dd312b2-117c-4a12-bd72-cee0914adf9d" />

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

<img width="491" height="181" alt="image" src="https://github.com/user-attachments/assets/435dbf1b-6fd4-475c-a374-382cbfd29c7e" />

#### Manual Calculations

<img width="363" height="244" alt="image" src="https://github.com/user-attachments/assets/1f130108-8e51-4900-beab-7efe971864ab" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="663" height="292" alt="image" src="https://github.com/user-attachments/assets/ccbbae80-82a1-4a5b-8e5f-10208d388063" />

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

<img width="487" height="189" alt="image" src="https://github.com/user-attachments/assets/ab8d1f90-1571-4026-ba1b-ea8dd1d675af" />


#### Manual Calculations

<img width="244" height="119" alt="image" src="https://github.com/user-attachments/assets/df79ff39-59a1-49a5-892f-524565419d7b" />


---
## OUTPUT FROM MASM SOFTWARE

<img width="655" height="400" alt="image" src="https://github.com/user-attachments/assets/44c3d53c-2083-43dc-9434-a2e4695c61bc" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

