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
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: R.LOGA MITHRA
RegisterNumber:212223100027

HALF ADDER:
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

FULL ADDER:
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire x,p,q,r;
xor(x,b,c);
xor(sum,x,a);
and(p,a,b);
and(q,b,c);
and(r,a,c);
or(carry,p,q,r);
endmodule
```
### Truth Table
HALF ADDER

![image](https://github.com/mithra916/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149986612/89b8a438-c031-4e4c-a035-38a4b730d243)

FULL ADDER

![image](https://github.com/mithra916/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149986612/66380191-9004-44b9-ad6f-16f9a93b967a)

RTL realization
### Output:
### RTL
HALF ADDER

![image](https://github.com/mithra916/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149986612/5bb88b87-b00b-49c0-ad0c-c223fac11282)

FULL ADDER

![image](https://github.com/mithra916/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149986612/058ef2b2-06a8-423d-8d8f-c45c12ed24d1)

### TIMING DIAGRAM
HALF ADDER

![halfadder EX NO 3(1)](https://github.com/mithra916/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149986612/c751527d-1603-4827-b645-eac1d72b83f2)

FULL ADDER

![fulladder EX NO 3(2)](https://github.com/mithra916/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149986612/6d126e24-0734-4d72-90d4-58e2aa743f25)


### Result:
```
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
```
