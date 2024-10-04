# EXP NO-4 FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Truthtable for full adder:**

![image](https://github.com/Meenu2823/FULL_ADDER_SUBTRACTOR/assets/139416219/d31dbfab-c7ae-4029-9f0e-071e3f8775f9)

**Truthtable for full subtractor:**

![image](https://github.com/Meenu2823/FULL_ADDER_SUBTRACTOR/assets/139416219/2d46d2d0-0df5-4d82-be7e-cfed7826a897)

**Procedure**

1.Open Quartus II and create a new project. 

2.Use schematic design entry to draw the full adder and full subtractor circuit.

3.The circuit consists of XOR, AND, and OR gates. 

4.Compile the design, verify its functionality through simulation. 

5.Implement the design on the target device and program it.

**Program:**
~~~
/* Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: SUNIL KUMAR T
RegisterNumber: 212223240164
*/

module FullAddSub(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule
~~~
![image](https://github.com/Meenu2823/FULL_ADDER_SUBTRACTOR/assets/139416219/69b6f66e-0798-4e7f-b2cb-5eee574fc626)

**RTL Schematic**
![Screenshot 2024-03-26 093911](https://github.com/Meenu2823/FULL_ADDER_SUBTRACTOR/assets/139416219/965a6daf-5ab7-47a8-bee5-83bab84bdbc3)

**Output Timing Waveform**
![Screenshot 2024-03-26 094510](https://github.com/Meenu2823/FULL_ADDER_SUBTRACTOR/assets/139416219/c450f0f8-ae98-4983-b1e5-4b44a57afa65)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
