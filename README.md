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
i)FULL ADDER

<img width="781" alt="Screenshot 2024-11-29 at 7 45 10 PM" src="https://github.com/user-attachments/assets/37c65e89-80b6-4edd-82d8-ae786043fdb8">

ii)FULL SUBTRACTOR

<img width="787" alt="Screenshot 2024-11-29 at 7 48 00 PM" src="https://github.com/user-attachments/assets/ee87a839-25cd-40b1-ae8e-7b702da30d28">

**Procedure**


1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**
i)FULL ADDER

```
module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));

endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Prathik T.S

RegisterNumber: 24000205

*/

**RTL Schematic**

FULL ADDER

<img width="1470" alt="Screenshot 2024-11-29 at 7 20 00 PM" src="https://github.com/user-attachments/assets/cf94ce51-daf9-4af6-9ec2-12e1169b4c08">

FULL SUBTRACTOR

<img width="1458" alt="Screenshot 2024-11-29 at 7 01 43 PM" src="https://github.com/user-attachments/assets/7e654765-a97e-4c98-881a-9d9891e22edc">

**Output Timing Waveform**

FULL ADDER

<img width="1465" alt="Screenshot 2024-11-29 at 11 18 15 PM" src="https://github.com/user-attachments/assets/232381c5-5ec5-4d3e-9ac5-8f8d6d8f61a0">

FULL SUBTRACTOR

<img width="1467" alt="Screenshot 2024-11-29 at 11 23 01 PM" src="https://github.com/user-attachments/assets/bb69b2c2-2dce-427e-95c6-26c9cd7c9130">


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



