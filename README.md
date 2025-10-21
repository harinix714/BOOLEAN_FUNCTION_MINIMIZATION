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

<img width="1920" height="1080" alt="Screenshot 2025-10-21 215545" src="https://github.com/user-attachments/assets/f7110d9b-46b8-4fba-9331-f9a0b149e9fb" />


**Output:**

**RTL**

<img width="1920" height="1080" alt="Screenshot 2025-10-21 215719" src="https://github.com/user-attachments/assets/348f3da0-eed8-441f-b8a0-a2b63efbab35" />


**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

