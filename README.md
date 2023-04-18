# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

## Implementation-of-Half-Adder-and-Full-Adder-circuit
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

#### Figure -01 HALF ADDER 
 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)


#### Figure -02 FULL ADDER 

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)



### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
### Half Adder
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sanjay Ragavendar Ragavendar
RegisterNumber:  212222100045
*/

module half_adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### Full Adder
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sanjay Ragavendar Ragavendar
RegisterNumber:  212222100045
*/

module full_adder(x,y,z,s,c);
input x,y,z;
output s,c;
wire x1,x3,x4;
xor(x1,x,y);
xor(s,x1,z);
and(x3,x,y);
and(x4,x,y);
or(c,x3,x4);
endmodule
```
Logic symbol & Truthtable
RTL realization

### Output:
### RTL
### HALF ADDER
![half_adder_RTL](https://user-images.githubusercontent.com/91368803/232842428-9b75e15d-4c37-4e72-896a-4be6e1d6e2e7.png)
### FULL ADDER
![full adder_RTL](https://user-images.githubusercontent.com/91368803/232842480-01beb893-bd2f-4b7a-bd16-45ce370f6f63.png)

### TIMING DIAGRAM
### HALF ADDER
![half_adder waveform](https://user-images.githubusercontent.com/91368803/232842570-617d5c78-c408-4a2f-ae52-127110879237.png)

### FULL ADDER
![full_adder waveform](https://user-images.githubusercontent.com/91368803/232842583-f8b82047-4216-42f8-809b-d6034d2c8e0e.png)

### TRUTH TABLE 
### HALF ADDER
![Half-adder-Truth-Table](https://user-images.githubusercontent.com/91368803/232842675-531560c1-a798-41cb-b189-cd59c43b3651.png)
### FULL ADDER
![Full-adder-Truth-Table](https://user-images.githubusercontent.com/91368803/232842712-081d34ed-edd7-481e-822e-4c72734ea33b.png)

### Result:
Thus the output of half_adder and full_adder experiment successfully achieved.
