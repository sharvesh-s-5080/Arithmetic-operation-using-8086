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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|    1200:12	           |      1204:24
1201:34	                 |     1205:68
1202:12	                 |
1203:34                   |                          |

#### Manual Calculations

![WhatsApp Image 2025-08-24 at 19 46 45_18f89076](https://github.com/user-attachments/assets/57ac5d4c-a5ee-4bec-83b2-383397388873)

---

## OUTPUT IMAGE FROM MASM SOFTWARE


<img width="640" height="480" alt="480816834-4ee570b4-7fa7-4e48-a792-70681c15d936" src="https://github.com/user-attachments/assets/f269a85d-039d-4f9a-bf33-9d29b013dfab" />

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
ADD AX,BX
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|           1200:12	     |     1204:00
   1201:34	              |     1205:00
   1202:12	              |
   1203:34                |                          |

#### Manual Calculations

![WhatsApp Image 2025-08-24 at 19 56 07_d17ee803](https://github.com/user-attachments/assets/b17ad98f-e445-4649-8425-8db257fa0f69)

---


## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="640" height="480" alt="480818151-da81f21e-4259-46f4-a6c8-d7da2fadeaf1" src="https://github.com/user-attachments/assets/4f3e2e36-8b77-4724-a2fd-848232009fd7" />



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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12	        |     1204:44
1201:34	                 |   1205:51
1202:12	                 |           1206:97
1203:34                   |          1207:0A                |

#### Manual Calculations


![WhatsApp Image 2025-08-24 at 20 08 38_28233bca](https://github.com/user-attachments/assets/296cfd05-d28d-4f14-ab42-798238d811f8)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="480822696-ab664247-a39e-44f7-846c-1504a88d0f37" src="https://github.com/user-attachments/assets/7b7ff586-b692-4a1a-8faa-69316895c27d" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200:12	        |
1201:34	                  |      1204:01
1202:12	                   |     1205:00
1203:34	                |      1206:00              |

#### Manual Calculations


![WhatsApp Image 2025-08-24 at 20 15 08_d4d0ec5d](https://github.com/user-attachments/assets/246de7f4-e252-4b39-8555-f23559fb68d5)

---
## OUTPUT FROM MASM SOFTWARE

<img width="640" height="480" alt="480824850-29be2be7-0f67-457c-8062-0892fbdaf1ce" src="https://github.com/user-attachments/assets/bc791895-60a9-429a-8d4f-c6d74f2a56d7" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
