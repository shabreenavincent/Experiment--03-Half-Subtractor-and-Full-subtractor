# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule


Developed by:shabreena vincent 
RegisterNumber: 22009378
*/

logic gates:
![logic gates exp03](https://user-images.githubusercontent.com/119475721/212972653-a645095a-d718-4332-840a-ed6580832fd1.png)






OUTPUT RTL REALIZATION

HALF SUBTRACTOR





![rtl output half subtractor](https://user-images.githubusercontent.com/119475721/212972697-595a404f-55b7-4cec-865e-df370e99c7a5.png)


FULL SUBTRACTOR



![rtl output full subtractor](https://user-images.githubusercontent.com/119475721/212972733-d4cec5b4-c522-413b-afd8-5d59fba00d7b.png)



TIMING DIAGRAM

HALF SUBTRACTOR




![timing diagram halfsubtractor](https://user-images.githubusercontent.com/119475721/212972765-df98d0e1-f347-4804-9e33-dc34da87cadd.png)




FULL SUBTRACTOR





![timing diagram full subtractor](https://user-images.githubusercontent.com/119475721/212972782-e47968c8-597b-4f18-8333-5bb4b2e35128.png)


Truthtable

HALF SUBTRACTOR




![truthtable half subtractor](https://user-images.githubusercontent.com/119475721/212972810-c0a4d387-50ed-40a0-ba4e-5f8ddf74b11b.png)


FULL SUBTRACTOR



![truthtable full subtractor](https://user-images.githubusercontent.com/119475721/212972826-af5c7a4b-dbb0-4e45-8bcb-822ef582617a.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
