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

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.



## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Developed by: anbuselvam .A
RegisterNumber:  212222240009

VERILOG PROGRAMMING FOR HALF SUBTRACTOR:
module halfsub(A,B,diff,borrow);

input A,B; output diff,borrow;

wire X;

xor(diff,A,B);

not(X,A);

and(borrow,X,B);

endmodule

VERILOG PROGRAMMING FOR FULL SUBTRACTOR:

module fullsub(A,B,C,diff,borrow);

input A,B,C;

output diff,borrow;

wire p ;

assign diff = A ^ B ^ C;

not(p,A);

assign borrow = ((p&B)|(p&C)|(B&C));

endmodule
```

*/

## Output:
HALF-SUBRACTOR:

## Truthtable
![01 (1)](https://user-images.githubusercontent.com/119559871/233828462-514f43fa-c131-4bc5-ad29-529a67086727.png)


##  RTL realization
![02 (1)](https://user-images.githubusercontent.com/119559871/233828554-e20517b9-06b2-45a5-97c5-e236b3ad1bd8.png)

## Timing diagram 
![03 (1)](https://user-images.githubusercontent.com/119559871/233828600-e8dac6ac-cabb-466e-a461-cdef71b08360.png)

FULL-SUBRACTOR:
## Truthtable
![04 (1)](https://user-images.githubusercontent.com/119559871/233828664-13d8c2b8-6099-47cd-a559-30de37635cd7.png)


##  RTL realization
![05 (1)](https://user-images.githubusercontent.com/119559871/233828707-fc828759-d59a-4011-8017-424760f42edc.png)

## Timing diagram 
![06 (1)](https://user-images.githubusercontent.com/119559871/233828740-63fa5bad-62e8-43eb-909e-d23ba201fc88.png)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
