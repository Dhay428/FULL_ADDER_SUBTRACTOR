![IMG-20241208-WA0029](https://github.com/user-attachments/assets/9d481f16-b7c6-4e75-9b0c-54319ef39ba3)# FULL_ADDER_SUBTRACTOR

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


![IMG-20241208-WA0030](https://github.com/user-attachments/assets/e24041e5-b115-445d-8508-a7ea6d64522f)

FULL SUBTRACTOR 
![IMG-20241208-WA0029](https://github.com/user-attachments/assets/0bedf8f1-f800-48ec-8077-f131d95db2ca)


**Procedure**

1 Type the program in Quartus software.

2 Compile and run the program.

3 Generate the RTL schematic and save the logic diagram.

4 Create nodes for inputs and outputs to generate the timing diagram.

5 For different input combinations generate the timing diagram



**Program:**
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
```

 Developed by:S.Dhayalaprabu
 
 RegisterNumber:24006289


**RTL Schematic**

FULL ADDER

![IMG-20241208-WA0031](https://github.com/user-attachments/assets/39cfb99b-aa70-47a5-86ed-03c4bcdbbf43)

FULL SUBTRACTOR

![IMG-20241208-WA0032](https://github.com/user-attachments/assets/3a13e1d8-895f-47b4-98a7-af53d3a94952)

**Output Timing Waveform**

FUNCTION 1
![IMG-20241208-WA0033](https://github.com/user-attachments/assets/8e47421c-b01a-44ca-a30e-f91eee82b07b)

FUNCTION 2
![IMG-20241208-WA0037](https://github.com/user-attachments/assets/9c010d2e-e201-4a67-917c-29bbbe856cb9)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



