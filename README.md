# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
Step 1: Create a project with required entities.
Step 2: Create a module along with respective file name.
Step 3: Run the respective programs for the given boolean equations.
Step 4: Run the module and get the respective RTL outputs.
Step 5: Create university program(VWF) for getting timing diagram.
Step 6: Give the respective inputs for timing diagram and obtain the results.
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: M SRINATH
RegisterNumber: 212222230147
USING NAND OPERATION
module fourexp(A,B,C,D,F);  
input A,B,C,D;  
output F;  
wire P,Q,R;  
assign P = C&(~B)&(~A);  
assign Q = D&(~C)&(~A);  
assign R = (~C)&B&(~A);  
assign F = (~P&~Q&~R);  
endmodule  
USING NOR OPERATION
module fourexp(A,B,C,D,F);  
input A,B,C,D;  
output F;  
wire P,Q,R,S;  
assign P = C&(~B)&A;  
assign Q = D&(~C)&A;  
assign R = C&(~B)&A;  
assign S = ~(P|Q|R);  
assign F = ~S;  
endmodule  
*/
## RTL realization

## Output:
## RTL FOR NAND ![image](https://user-images.githubusercontent.com/123470785/214344822-b443edee-f040-41e8-90ab-10ae49bf8791.png)
FOR NOR ![image](https://user-images.githubusercontent.com/123470785/214345105-928992f9-cca2-4f47-b58c-8b44a6ea292f.png)
## Timing Diagram FOR NAND ![image](https://user-images.githubusercontent.com/123470785/214345368-9f9d1b67-1387-4696-9882-22de0925401b.png)
FOR NOR 
![image](https://user-images.githubusercontent.com/123470785/214345574-c81b6138-4244-40af-8bf3-aa13399349a5.png)

Truth Table: FOR NAND ![image](https://user-images.githubusercontent.com/123470785/214346012-7c77b780-b81e-462f-a5b1-769339ea79fc.png)
FOR NOR
![image](https://user-images.githubusercontent.com/123470785/214346425-988f69ea-2c0e-4970-9c3c-c2a9b2dee8e8.png)
## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
