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

![afd256d4-223a-4987-9b68-2e202c1175f3](https://github.com/user-attachments/assets/f2bbe3f4-7546-4435-91e9-37a80526eaba)

FULL SUBTRACTOR

![b93bfb65-3983-4dea-b856-0f40e80e79ea](https://github.com/user-attachments/assets/8da1a079-713b-4939-a785-e1f44c07eaaf)


**Procedure**

1)Type the program in Quartus software.

2)Compile and run the program.

3)Generate the RTL schematic and save the logic diagram.

4)Create nodes for inputs and outputs to generate the timing diagram. 

5)For different input combinations generate the timing diagram



**Program:**

FULL ADDER

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


![Screenshot 2024-11-14 225122](https://github.com/user-attachments/assets/58dfe094-0925-4ddf-87d6-14acee1d8f5d)


FULL SUBTRACTOR


![Screenshot 2024-11-15 004622](https://github.com/user-attachments/assets/a113383a-75a3-4845-8778-4303ec641883)

**Output Timing Waveform**

FULL ADDER


![Screenshot 2024-11-14 230044](https://github.com/user-attachments/assets/3e4d880d-ce24-4787-a8b0-309c78140efd)


FULL SUBTRACTOR

![Screenshot 2024-11-14 222509](https://github.com/user-attachments/assets/ee389451-ac74-4abd-af27-43b44f51ec0a)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



