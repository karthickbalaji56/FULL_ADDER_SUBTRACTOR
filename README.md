# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

Developed by:Karthick Balaji S
RegisterNumber: 212225040174

```
module fulladdersub(
   input A, B, Cin,
   output SUM, CARRY, BO, DIFF
);

assign SUM = A ^ B ^ Cin;
assign CARRY = (A & B) | (B & Cin) | (A & Cin);

assign DIFF = A ^ B ^ Cin;
assign BO = (~A & B) | (~A & Cin) | (B & Cin);
endmodule
```
<img width="929" height="518" alt="image" src="https://github.com/user-attachments/assets/72dabafb-7e2d-43d0-af85-c5ac3a9d65dd" />

**RTL Schematic**
<img width="928" height="522" alt="image" src="https://github.com/user-attachments/assets/2f53d036-63fe-4b3b-b7b6-d3c2de46ed7e" />



**Output Timing Waveform**
<img width="918" height="519" alt="image" src="https://github.com/user-attachments/assets/8edfe789-7bc4-4350-a301-d10cce1442b9" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



