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

![c1f0e3c3-bfe7-4a74-9988-2546ce86fd0a](https://github.com/user-attachments/assets/e3f21e0c-f58a-4569-9a2e-0aae5d8976d2)

FULL SUBTRACTOR

![aff6b799-44a2-45b9-a85c-5f561ae29b9b](https://github.com/user-attachments/assets/e26484cc-bddb-4eb4-a453-5ca864c1c487)


**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**

FULL ADDER
```
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
```

FULL SUBTRACTOR
```
module exp4a(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Kiruba RC RegisterNumber:24900445
*/

**RTL Schematic**

FULL ADDER
![63c1e0be-a241-43da-817b-c48a8c510e2e](https://github.com/user-attachments/assets/16134394-9207-488a-aa1e-3fb6df18b9f2)

FULL SUBTRACTOR
![5bc65426-0a89-47f1-b935-365771a06b98](https://github.com/user-attachments/assets/d9c9cf56-0bc1-4d31-844c-30d71fa09dc3)



**Output Timing Waveform**

FULL ADDER

![c69df30b-f5ed-4036-9ac3-3273a4bdb223](https://github.com/user-attachments/assets/3a7bcc51-91f3-4893-ad26-07b08cb79acf)


FULL SUBTRACTOR

![c1ec79db-7e01-4de9-a889-7f23dec209b5](https://github.com/user-attachments/assets/37e6c4bd-daab-4ad6-9ad5-36b7cc91f637)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



