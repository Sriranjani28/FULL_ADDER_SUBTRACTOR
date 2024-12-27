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
FULL ADDER
<img width="275" alt="ex 4 truth table(full adder)" src="https://github.com/user-attachments/assets/f9ddc6fe-1832-480f-a599-59d1b788ec7e" />
FULL SUBTRACTOR
<img width="288" alt="ex 4 truth table(full subtractor)" src="https://github.com/user-attachments/assets/90baa0fd-068c-4d5e-9ca3-92b0741c78c8" />


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
FULL ADDER

module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule

FULL SUBTRACTOR

module experiment4a (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(-w1&bin);
assign df-w1^bin;
assign bo-w2/w3;
endmodule
Developed by: Sriranjani.M
RegisterNumber:24900016
*/

**RTL Schematic**
FULL ADDER
<img width="565" alt="ex 4" src="https://github.com/user-attachments/assets/39297a09-1d69-4db0-a524-db3b36180784" />

FULL SUBTRACTOR
<img width="658" alt="ex 4 full subtractor" src="https://github.com/user-attachments/assets/ced7df62-ab1f-4aeb-97a5-b2a01966368e" />




**Output Timing Waveform**
FULL ADDER
<img width="623" alt="ex 4 timing diagram(full adder)" src="https://github.com/user-attachments/assets/f84923a3-2438-442c-9e6f-09d54fbd1240" />

FULL SUBTRACTOR
<img width="619" alt="ex 4 timing diagram(full subtractor)" src="https://github.com/user-attachments/assets/921c2889-f468-4aa7-86e6-f94a5bf5f83e" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



