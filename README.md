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

![WhatsApp Image 2024-11-15 at 13 54 59_a085e6bd](https://github.com/user-attachments/assets/b24517c7-a5fa-426e-89c5-4099b9d50246)

FULL SUBTRACTOR

![WhatsApp Image 2024-11-15 at 13 54 59_dbc02022](https://github.com/user-attachments/assets/2017b371-d8f7-4a4d-8c3b-8e54d3da19e3)


**Procedure**

1)Type the program in Quartus software.

2)Compile and run the program.

3)Generate the RTL schematic and save the logic diagram.

4)Create nodes for inputs and outputs to generate the timing diagram. 

5)For different input combinations generate the timing diagram.



**Program:*

FULL ADDER

```
module exp6(df,bo,a,b,bin);
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






FULL SUBTRACTOR
```
module exp6(df,bo,a,b,bin);
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

Developed by: LOKESH S

RegisterNumber: 24009455

**RTL Schematic**
FULL ADDER
![Screenshot 2024-11-15 132227](https://github.com/user-attachments/assets/f6fde0b1-a479-43e5-b3f2-68fe4e8fcd4c)

FULL SUBTRACTOR

![Screenshot 2024-11-15 135116](https://github.com/user-attachments/assets/8c22f790-14cd-4925-88ae-4f2df745141b)




**Output Timing Waveform**
FULL ADDER
![Screenshot (9)](https://github.com/user-attachments/assets/00e5763f-2de1-4918-9ea9-bc8485fc67e8)

FULL SUBTRACTOR

![Screenshot (10)](https://github.com/user-attachments/assets/34c4666c-1712-4975-a8c9-2196469c24a2)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



