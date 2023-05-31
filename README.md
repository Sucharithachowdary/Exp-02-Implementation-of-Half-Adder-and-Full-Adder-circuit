# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: sucharitha.k
RegisterNumber:  212221240021
*/
### HALF ADDER:
~~~
module ex2(A,B,Cin,S,Cout); 
input A,B,Cin;
output S,Cout; 
wire D,E,F;
xor(D,A,B);
xor(S,D,Cin); 
and(E,Cin,D);
and(F,A,B); 
or(Cout,E,F);
endmodule
~~~
### FULL ADDER
~~~
module ex2(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
~~~
### Output:
### logic symbol
![output](https://github.com/Sucharithachowdary/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/blob/main/logic%20symbol.png)
### HALF ADDER
### TRUTH TABLE
![232230888-3439e1dc-17e7-4223-99c3-caa6fdbfbd91](https://user-images.githubusercontent.com/94166007/233142013-c80c5910-80d2-4c9a-8d55-21bd9ff1008a.png)

### RTL
![232230895-623408fa-19ed-4e0c-a232-2198d7283eab](https://user-images.githubusercontent.com/94166007/233142056-fc3ba256-32b6-454f-8a2d-a2df898d7357.png)

### TIMING DIAGRAM
![232230907-aee7a28a-16a1-45c0-aef2-4498d9df097e](https://user-images.githubusercontent.com/94166007/233142077-07188412-2089-435d-9c67-a03f94043cd6.png)

### FULL ADDER
![232230923-248fa731-31ca-4b07-b76d-c0c4c8b4fa49](https://user-images.githubusercontent.com/94166007/233142156-b794ba87-9f3b-4947-a72a-4625c8aeebd6.png)

### RTL

![232230950-8135a8b3-31fa-4b28-87a4-0ffad4e56872](https://user-images.githubusercontent.com/94166007/233142305-59c4bf0c-1ad5-481f-83a1-663f4dbadb98.png)

### TIMING DIAGRAM
![232230950-8135a8b3-31fa-4b28-87a4-0ffad4e56872](https://user-images.githubusercontent.com/94166007/233142391-03194506-e424-4895-a35a-580948990a82.png)



### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
