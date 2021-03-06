## Quadratic Optimization 

This directory is dedicated to self-study on a quadratic optimization problem using a quantum annealer. 

There are four input files 
example_0/1/2/3.txt 

These are the only input, and the form of quadratic function is determined based on the input. 
First of all, the content of each file is like following, example_0.txt for example 

     1   1   -2.0
     3   3   3.0
     2   3   -1.0

The first two columns are indices of variables, and then the total number of to-be-determined variables is 3 
as it is the largest number in the first two colums. The third column indicate coefficients of the quadratic function. 

Then the objective function for this example can be written as follow

<img src="https://www.codecogs.com/eqnedit.php?latex=H(x_1,x_2,x_3)&space;=&space;-2x_1&space;&plus;&space;3x_3&space;-x_2x_3" target="_blank"><img src="https://latex.codecogs.com/gif.latex?H(x_1,x_2,x_3)&space;=&space;-2x_1&space;&plus;&space;3x_3&space;-x_2x_3" title="H(x_1,x_2,x_3) = -2x_1 + 3x_3 -x_2x_3" /></a>

Each variable can only have either 0 or 1, and then there will be 2^3(=8) possible combinatorial solutions. For this case, there are eight possible combinations as
<img src="https://www.codecogs.com/eqnedit.php?latex=(x1,x2,x3)=&space;000/111/001/110/010/101/100/011" target="_blank"><img src="https://latex.codecogs.com/gif.latex?(x1,x2,x3)=&space;000/111/001/110/010/101/100/011" title="(x1,x2,x3)= 000/111/001/110/010/101/100/011" /></a>

The optimal solution minimizes the objective function H.  


In this directory, I implemented this quadratic optimization in two ways
1. exact enumeration (effective for small number of variables)
2. Monte Carlo method (for larger number of variables)
