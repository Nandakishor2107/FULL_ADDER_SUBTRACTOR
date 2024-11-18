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

Developed by: NANDA KISHOR SURESH PRIYA

RegisterNumber: 24011485
*/


//Full Adder

```
module fulladder(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;

wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule
```

//Full Subtractor

```
module fullsubractor(a, b, cin, diff, borrow);
 input a;
 input b;
 input cin;
 output diff;
 output borrow;
wire abar;
assign abar= ~ a;
assign diff=a^b^cin;
assign borrow=(abar & b) | (b & cin) |(cin & abar);
endmodule

```
**RTL Schematic**

//Full Adder

![fa-lg](https://github.com/user-attachments/assets/0fffd534-7c5a-4805-97c3-e2642af06d2a)


//Full Subtractor

![fs-lg](https://github.com/user-attachments/assets/a10c16ef-107b-458e-9ac5-a9d63ce97f9e)


**Output Timing Waveform**

//Full Adder

![fa-wf](https://github.com/user-attachments/assets/ec17f64f-d043-4633-9ab4-966ed67c8102)

//Full Subtractor

![fs-waverform](https://github.com/user-attachments/assets/3f00a875-4e32-42d2-b7a9-c1f40e47d66f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



