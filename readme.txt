4 bit Arithmetic Unit - EC372 VLSI Design Lab Project
Done by:
16EC105 - Anirudh BH
16EC118 - Manan Sharma

The circuit consists of a 4x4 multiplier, 4 bit adder and subtracter. It has ports cin, sel, a(a_3, a_2, a_1, a_0), b(b_3, b_2, b_1, b_0) as inputs and gives out_7, out_6, out_5, out_4, out_3, out_2, out_1, out_0. 

The operation is as follows

|sel|cin|operation|
|---|---|---------|
| 0 | X |   a*b   |
| 1 | 0 |   a+b   |
| 1 | 1 |   a-b   |

During multiplication operation, all 8 bits of the output are valid. During addition/subtraction, only out_3, out_2, out_1, out_0 are valid, and out_5 represents the cout.

Details
Area = 992 x 642 = 636864 square microns
Worst Case Dynamic Power consumed = 1.39019 mW 
Delay = 13.6 ns (worst case)
No of cells = 76
Sum of nodal capacitances = 27.359362 pF

The submission folder contains .mag file, .sim file, and a python script called test.py that will generate the .cmd file containing all possible test vectors.

Python Script Usage
python3 test.py Arithemtic_Unit.sim
The python script will write the .cmd file. Once written, irsim will automatically be called and its outputs will be stored in output.log file. Then, the python script will read the .log file, and evaluate the accuracy of the circuit. It also computes the maximum dynamic power dissipated, and capacitance and display it.
