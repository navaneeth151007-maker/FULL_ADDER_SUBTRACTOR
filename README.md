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
Full add
![WhatsApp Image 2025-11-19 at 11 34 35_46047c98](https://github.com/user-attachments/assets/513e2af9-d730-41ab-a760-30d33ce5ad58)

Full Sub
![WhatsApp Image 2025-11-19 at 11 35 14_6fdd929d](https://github.com/user-attachments/assets/7d268bc3-fd1a-4a4f-9d96-415610d488e9)

**Procedure**
Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**
Full add
```
module exp2(a,b,c,S,C);
input a,b,c;
output S,C;
xor g1(S,a,b);
assign C=(a&b)|(b&c)|(c&a);
endmodule
```
Full sub
```
module exp2(a,b,bin,dif,bout);
input a,b,bin;
output dif,bout;
assign dif=a^b^bin;
assign bout=(a&b)|(bin&(a^b));
endmodule
```
**RTL Schematic**
full add
<img width="1920" height="1080" alt="exp 4 add rtl" src="https://github.com/user-attachments/assets/a7f730eb-ed80-4f56-9416-a7e42761f72f" />

full sub
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f17bf3f7-4c81-42f1-aeed-3ab35ef2d4ef" />



**Output Timing Waveform**
Full add
![exp 4 add out](https://github.com/user-attachments/assets/4e8f5ff7-60a3-4280-85c5-b2f3affee3e3)

Full sub
![exp 4 sub out](https://github.com/user-attachments/assets/7dd81a7f-8bec-400e-8922-7f85656f7a89)


**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



