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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

```
module Day3(A,B,C,Sum,Carry);
input A,B,C;
output Sum,Carry;
xor g1(Sum,A,B);
assign Carry=(A&B)|(B&C)|(C&A);
endmodule

module DAY4 (A,B,C,Di,Bo) ;
input A,B,C ;
output Di,Bo ;
xor g1 (Di,A,B,C) ;
assign Bo = (~A&C)|(B&C)|(~A&B) ;
endmodule
```


**RTL Schematic**
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/553a7a3f-d74f-42ae-965e-ce5042fa51ed" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a09a712e-1a83-4dc5-8c85-f50ba852f4e2" />

**Output Timing Waveform**

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a72c40cf-ee66-40d1-b930-c8483b6bec7d" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a4c6ed6a-baec-4886-b80b-01b75352ee2a" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



