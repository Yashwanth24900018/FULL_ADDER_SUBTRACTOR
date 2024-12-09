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

**Fulladder**

![Screenshot 2024-12-09 133249](https://github.com/user-attachments/assets/e490177d-a84e-436f-974d-f682a984891d)

**Fullsubractror**

![Screenshot 2024-12-09 133427](https://github.com/user-attachments/assets/05000369-8465-45c8-9470-8c58744516be)



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:yashwanth.asv RegisterNumber:24900018
*/

 Full adder



 
    module fa(a,b,cin,sum,carry);
    input a,b,cin;
    output sum,carry;
    assign sum=( (a ^ b)^cin);
    assign carry= ( (a & b)| ( cin &(a ^ b )));
    endmodule
 
 
 
 
 Full subtractor
 
 
 
 
    module fs(a,b,bin,difference,borrow);
    input a,b,bin;
    4/6
    output difference,borrow;
    assign difference= ( (a ^ b)^bin);
    assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
    endmodule

**RTL Schematic**

![Screenshot 2024-12-09 133710](https://github.com/user-attachments/assets/547aeeee-16c7-45df-b7be-75e59c1c93da)


**Output Timing Waveform**

![Screenshot 2024-12-09 133754](https://github.com/user-attachments/assets/44b7fe9c-c2d2-40ef-867e-d022392e934d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



