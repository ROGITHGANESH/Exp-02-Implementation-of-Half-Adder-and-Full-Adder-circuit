# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

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
# half_adder
```
module half_adder(a,b,s,c);
output s,c;
input a,b;
assign s=a^b;
assign c=a&b;
endmodule
```

# full_adder
```
module full_adder(A,B,cin,S,cout);
input A,B,cin;
output S,cout;
assign S=A^B^cin;
assign cout=(A&B)| (B&cin)| (A&cin);
endmodule
```
Logic symbol & Truthtable
RTL realization

### Output:
half_adder
![image](https://github.com/ROGITHGANESH/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152588322/ca86485d-b49b-49a7-8269-ba6bf1a9fc2b)
full_adder
![image](https://github.com/ROGITHGANESH/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152588322/d69639a9-47b8-47a1-9a97-98a1d32ff176)

### RTL
# half_adder
![image](https://github.com/ROGITHGANESH/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152588322/b2c606c5-288e-4fa7-8b7f-50ad02501255)
# full _adder
![image](https://github.com/ROGITHGANESH/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152588322/b86bd8e8-9ee5-4a1a-a7c6-4605db0a9a58)

### TRUTH TABLE 
# half_adder
![image](https://github.com/ROGITHGANESH/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152588322/208169a1-84c7-473b-948d-555fc9710de6)

# full_adder
![image](https://github.com/ROGITHGANESH/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152588322/97c929fe-c008-4b57-bc62-da3b49827249)


### Result:
The program Half adder and full adder executed succesfully.
