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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:Mahalakshmi S
RegisterNumber:212225220060
*/
'''
module exp_3a(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule

FULL SUBTRACTOR:
module exp_3b(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule
'''

**RTL Schematic**
FULL ADDER
<img width="1461" height="818" alt="d4" src="https://github.com/user-attachments/assets/1751794d-8d66-44ce-a13e-cbe447e5a6a0" />
FULL SUBTRACTOR:
<img width="1460" height="816" alt="d 4 1" src="https://github.com/user-attachments/assets/9238dc6f-c969-4af6-9172-52e28c09aab9" />


**Output Timing Waveform**
FULL ADDER:
<img width="1463" height="825" alt="d4 2" src="https://github.com/user-attachments/assets/bcd2dd25-ecd5-43d3-b824-e522b3d3acc6" />
FULL SUBTRACTOR:
<img width="1460" height="816" alt="d4 3" src="https://github.com/user-attachments/assets/2438b4ff-ffda-44b2-a630-8425720333b3" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



