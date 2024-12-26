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

![Screenshot 2024-12-26 181030](https://github.com/user-attachments/assets/7051bc6e-f3df-4eaa-aa70-5c6cfb8020e7)

![Screenshot 2024-12-26 181035](https://github.com/user-attachments/assets/cd1edb83-1471-4f4e-a5b9-8b47511805f6)

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

    module halfadder(a,b,sum,carry);
    input a,b;                                     
    output sum,carry;                        
    assign sum=(a^b);
    assign carry=(a&b);
    endmodule

    module halfsub(a,b,difference,borrow);
    input a,b;
    output difference,borrow;
    assign difference=(a^b);
    assign borrow=(~a&b);
    endmodule
**RTL Schematic**

i)

![Screenshot 2024-12-26 181625](https://github.com/user-attachments/assets/83389c84-8cad-41a9-977c-e7dfa82780cf)

ii)

![Screenshot 2024-12-26 181636](https://github.com/user-attachments/assets/22101340-ceca-42e6-8653-1b75a4d0e0d7)

**Output/TIMING Waveform**

halfadder
![Screenshot 2024-12-01 105746](https://github.com/user-attachments/assets/22c5ff09-db72-47c1-9903-eaf093dfa475)
halfsub
![Screenshot 2024-12-01 110436](https://github.com/user-attachments/assets/b2a9fa13-236c-4eba-8236-5b53f1bb6b82)

**Result:**

 Thus the given Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

