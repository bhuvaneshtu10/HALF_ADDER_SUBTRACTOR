# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![Screenshot 2024-12-01 105508](https://github.com/user-attachments/assets/3b69e235-bcfc-4e2a-81ed-aad9a934db21)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 
![Screenshot 2024-12-01 110255](https://github.com/user-attachments/assets/4eb80610-96a0-431b-9dd9-ed8c28b19248)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:BHUVANESHWARAN TU
RegisterNumber:*/24009351 

**RTL Schematic**
half adder


      module halfadder(a,b,sum,carry);
      input a,b;                                     
      output sum,carry;                        
      assign sum=(a^b);
      assign carry=(a&b);
      endmodule

 halfsub
 
      module halfsub(a,b,difference,borrow);
      input a,b;
      output difference,borrow;
      assign difference=(a^b);
      assign borrow=(~a&b);
      endmodule

**truth table**

![Screenshot 2024-12-03 204839](https://github.com/user-attachments/assets/27b04a8b-0654-4ff4-9968-dfd96873b092)
![Screenshot 2024-12-03 204850](https://github.com/user-attachments/assets/301b34df-5234-4e24-ac8d-3c2190847076)

**Output/TIMING Waveform**
halfadder
![Screenshot 2024-12-01 105746](https://github.com/user-attachments/assets/22c5ff09-db72-47c1-9903-eaf093dfa475)
halfsub
![Screenshot 2024-12-01 110436](https://github.com/user-attachments/assets/b2a9fa13-236c-4eba-8236-5b53f1bb6b82)

**Result:**
half adder
![Screenshot 2024-12-01 105508](https://github.com/user-attachments/assets/c1c102d5-4d4b-4f2d-8502-7475b12881a6)
halfsub
![Screenshot 2024-12-01 110255](https://github.com/user-attachments/assets/3e64c7f8-0783-4d40-a819-e1ba9b9a9b27)

