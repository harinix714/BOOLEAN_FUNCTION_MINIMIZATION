# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:Harini S K
RegisterNumber:25018849

 module booleanexpression ( input A, B, C, D, output F );
 wire nB, nD, term1, term2, term3;
 // NOT gates
 not (nB, B);
 not (nD, D);
 // AND terms
 and (term1, nB, nD);   // B'D'
 and (term2, A, C);     
// AC
 and (term3, B, D);     
// BD
 // OR the terms
 or  (F, term1, term2, term3);
 
  endmodule
**RTL realization**
<img width="824" height="426" alt="Screenshot 2025-10-20 151527" src="https://github.com/user-attachments/assets/d4adac32-a147-4354-b7e6-6a603da2ef34" />

**Output:**

**RTL**
<img width="828" height="534" alt="Screenshot 2025-10-20 151543" src="https://github.com/user-attachments/assets/12e5888b-8572-462b-b667-1c94d8fb8066" />

**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

