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


<img width="464" height="203" alt="image" src="https://github.com/user-attachments/assets/4279ede9-aa0c-4b73-960f-e035be7478bf" />

FULL SUBTRACTOR

<img width="300" height="212" alt="image" src="https://github.com/user-attachments/assets/5063447b-3b24-4284-83f8-71aa2e15e907" />



**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

FULL ADDER
```
module fafs(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule
```
FULL SUBTRACTOR
```
module fullsub(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule
```

Developed by: INDUJA R RegisterNumber: 25001726
*/

**RTL Schematic**

FULL ADDER

<img width="1186" height="377" alt="Screenshot 2025-10-18 212017" src="https://github.com/user-attachments/assets/e6c20d7e-34ed-4755-8e75-01005b555125" />
FULL SUBTRACTOR

<img width="946" height="387" alt="Screenshot 2025-10-18 224402" src="https://github.com/user-attachments/assets/015f7282-f4cd-45bf-a147-df7d475c8d68" />



**Output Timing Waveform**
FULL ADDER

<img width="1919" height="1020" alt="Screenshot 2025-10-18 212326" src="https://github.com/user-attachments/assets/51552fbc-6f19-45be-ba17-f6026de58cc6" />

FULL SUBTRACTOR

<img width="1919" height="1014" alt="Screenshot 2025-10-18 224556" src="https://github.com/user-attachments/assets/14097ad9-896f-4dcd-8197-f9fc4fd29e3b" />

**Result:**


Thus, the Full Adder and Full Subtractor circuits are designed, and the truth tables are verified using Quartus software.



