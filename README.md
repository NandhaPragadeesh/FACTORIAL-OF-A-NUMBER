# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

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

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

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
OUTPUT
<img width="1919" height="1016" alt="Screenshot 2025-09-22 214729" src="https://github.com/user-attachments/assets/c0290a06-e0b3-47c2-b497-ed909b6aaf09" />
<img width="1506" height="597" alt="Screenshot 2025-09-22 215033" src="https://github.com/user-attachments/assets/ad30b942-50b5-41b5-bc91-27e1e8f40700" />


---
MANUAL CALCULATIONS
![WhatsApp Image 2025-09-22 at 22 25 53_7d149511](https://github.com/user-attachments/assets/0d4ad325-b988-4dd9-8ae2-86d623d4eb1d)
---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


