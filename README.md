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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. /*

Developed by:Sanjay S
RegisterNumber:25017293

```
module fulladd(input a,b,cin,output difference,borrow);

assign sum = a^b^cin;

assign carry=(a&b)|(b&cin)|(cin&a);

endmodule

modulefullsub(input a,b,bin,output difference,borrow);

assign difference=a^b^bin;

assign borrow =(~a&b)|(bin&~a)|(bin&~b);

endmodule
```


**RTL Schematic**


<img width="790" height="403" alt="image" src="https://github.com/user-attachments/assets/00681b5a-e570-423c-b988-c75b18881db0" />


<img width="819" height="420" alt="image" src="https://github.com/user-attachments/assets/c4be266d-c630-4e16-a841-5a3e47e6f057" />


**Output Timing Waveform**


<img width="798" height="425" alt="image" src="https://github.com/user-attachments/assets/45f9c07b-4f8b-4827-a0e0-eeee7e0c25f8" />


<img width="816" height="375" alt="image" src="https://github.com/user-attachments/assets/caf5f9c7-0b3f-44ef-baef-7b30fedd77ff" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



