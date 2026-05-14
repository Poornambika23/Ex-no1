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

<img width="846" height="448" alt="image" src="https://github.com/user-attachments/assets/69540cc7-ce53-4e11-aaf7-31aa33d00f92" />
              |

#### Manual Calculations

<img width="482" height="338" alt="image" src="https://github.com/user-attachments/assets/7818ae0c-8780-47c2-8125-962406ddfe7b" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="877" height="589" alt="image" src="https://github.com/user-attachments/assets/8a2ebe6c-01c1-4658-98c2-62d8ecf0acf1" />


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
<img width="703" height="392" alt="image" src="https://github.com/user-attachments/assets/1799e358-42e4-4179-bcee-56e62220db89" />


#### Manual Calculations
<img width="382" height="288" alt="image" src="https://github.com/user-attachments/assets/e2eabe20-eab9-4e2c-9d70-0597e2f135c2" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="869" height="611" alt="image" src="https://github.com/user-attachments/assets/d9afac40-0872-4591-9126-fbae00664ea7" />


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

<img width="680" height="363" alt="image" src="https://github.com/user-attachments/assets/fddd5abd-0f92-474b-9baf-8343e0ab578f" />


#### Manual Calculations

<img width="376" height="251" alt="image" src="https://github.com/user-attachments/assets/070fe401-db33-4f4e-8bc9-e1a99c0ba244" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="891" height="595" alt="image" src="https://github.com/user-attachments/assets/b90cc836-5a2e-4dd7-9185-860a73afea2e" />


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
<img width="674" height="359" alt="image" src="https://github.com/user-attachments/assets/f0c26949-d3c2-4a2b-b715-b9d841e42f13" />


#### Manual Calculations

<img width="413" height="267" alt="image" src="https://github.com/user-attachments/assets/ccf4fc3e-81d3-416b-b2bb-04bd08f561bc" />

## OUTPUT FROM MASM SOFTWARE
<img width="870" height="587" alt="image" src="https://github.com/user-attachments/assets/e4aede3a-33f5-4bcc-8260-95f8f5af180d" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

