# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

 AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

 APPARATUS REQUIRED

* Personal Computer with MASM Software

---

 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


 FLOW CHART
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
| 1200:12                 | 1200:24                  |
| 1201:34                 | 1205:68                  |
| 1202:12                 | 1206:00                  |
| 1203:34                 |                          |

 Manual Calculations

<img width="1163" height="1280" alt="image" src="https://github.com/user-attachments/assets/fc6da5b7-0166-442d-99dd-efa4b9382209" />


---

 OUTPUT IMAGE FROM MASM SOFTWARE

![WhatsApp Image 2025-11-17 at 21 33 35_91085ab3](https://github.com/user-attachments/assets/2c1c1af1-be03-41e1-8bd7-c0aa2a4f4b21)


 2. SUBTRACTION

 Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

 FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


 Program

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

 Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200:12                  | 1200:00                 |
| 1201:34                  | 1205:00                 |
| 1202:12                  | 1206:00                 |
| 1203:34                  |                         |


 Manual Calculations

<img width="1259" height="1280" alt="image" src="https://github.com/user-attachments/assets/48f564a3-3a52-4920-a0e0-fbe0c89ed943" />


---


 OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-11-17 at 21 39 25_1049ff75](https://github.com/user-attachments/assets/97dda6cd-7366-4ae2-9abd-3d3e3da25a43)



 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



 Program

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

 Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200:12                 | 1200:44                  |
| 1201:34                 | 1205:51                  |
| 1202:12                 | 1206:97                  |
| 1203:34                 | 1207:0A                  |


 Manual Calculations

<img width="1213" height="852" alt="image" src="https://github.com/user-attachments/assets/bf3d3352-0283-4463-9245-3e9d41ffe419" />


---

 OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-11-17 at 22 10 47_02da12cc](https://github.com/user-attachments/assets/82db77fa-4e93-4d44-b36d-8687e5ef9eb2)


 4. DIVISION

 Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

 FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


 Program

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

 Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200:12                 | 1200:01                  |
| 1201:34                 | 1205:00                  |
| 1202:12                 | 1206:00                  |
| 1203:34                 | 1207:00                  |


 Manual Calculations

<img width="1280" height="710" alt="image" src="https://github.com/user-attachments/assets/c31e4a68-10d8-4e18-80c6-d7b14453f8c8" />


---
 OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-11-17 at 22 10 46_8c5714a9](https://github.com/user-attachments/assets/344c6dd5-8ce2-43a6-9244-569d1180543c)


 RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
