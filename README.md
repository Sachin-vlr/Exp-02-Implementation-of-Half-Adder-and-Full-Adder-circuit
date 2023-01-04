# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime Theory Adders are digital circuits that carry out addition of numbers.

Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin


Figure -01 HALF ADDER
![halfadder](https://user-images.githubusercontent.com/113497666/210476754-832f0ac2-9e47-4da2-89da-b045849d536f.png)


Figure -02 FULL ADDER
![full](https://user-images.githubusercontent.com/113497666/210476804-8c09af34-e3de-45b4-839b-243a7522bfc6.png)


Procedure
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

Program:
```

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: SACHIN.C
RegisterNumber:  22001187

Program:
#Half adder :
module exptwo(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

#Full adder:
module expthree(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
Logic symbol & Truthtable
![logicgate](https://user-images.githubusercontent.com/113497666/210476088-d50330fd-2da7-4304-b7df-6ed899b2763a.jpg)

RTL realization

Output:
RTL
HALF ADDER

![half](https://user-images.githubusercontent.com/113497666/210476152-9d803e63-57a2-4f5a-8a0a-a75abeed8b2b.png)

FULL ADDER

![fulladder](https://user-images.githubusercontent.com/113497666/210476185-d85cf05b-b364-4104-880b-2caa7ae4dfa8.png)


TIMING DIAGRAM

![timing](https://user-images.githubusercontent.com/113497666/210476207-84835d9f-a94d-4b55-9866-a43772bed591.png)


TRUTH TABLE
![truth](https://user-images.githubusercontent.com/113497666/210476222-b86eb9f6-a4d1-4c1f-8ba6-1c2b160c9b58.png)


Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.
