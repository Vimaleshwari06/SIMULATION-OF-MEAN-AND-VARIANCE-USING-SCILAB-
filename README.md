# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-
__AIM:__

To write a program for mean, variance and cross correlation in SCILAB and verify the output. 

__EQUIPMENTS NEEDED:__

.Computer with i3 Processor 

.SCI LAB 

__ALGORITHM:__

1. Define the Function: Specify the function you want to simulate. For example, 
f(x)=sin⁡(x)f(x)=sin(x) or any other function. 
2. Generate Sample Points: Decide on the range and the number of sample points. Generate 
these sample points within the desired range. 
3. Evaluate the Function: Compute the function values at each of these sample points. 
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the 
mean and variance of the computed function values. 
5. Display Results: Output the computed mean variance and Cross Correlation 

__PROCEDURE:__ 

1.Refer Algorithms and write code for the experiment. 

2.Open SCILAB in System 

3.Type your code in New Editor 

4.Save the file 

5.Execute the code If any Error, correct it in code and execute again 
  
6.Verify the generated results

__PROGRAM:__
```
clear;
clc;
function X=f(x)
    z = 3*(1-x)^2; // Marginal PDF
    X = x*z;
endfunction
a = 1.5;
b = 2;
EX = intg(a, b, f); // Mean of X
function Y=c(y)
    z = 3*(1-y)^2; // Marginal PDF
    Y = y*z;
endfunction
EY = intg(a, b, c); // Mean of Y
disp(EX, "i) Mean of X =");
disp(EY, "Mean of Y =");
function X=g(x)
    z = 3*(1-x)^2;
    X = x^2*z;
endfunction
EX2 = intg(a, b, g);
function Y=h(y)
    z = 3*(1-y)^2;
    Y = y^2*z;
endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2; // Variance of X
vY2 = EY2 - (EY)^2; // Variance of Y
disp(vX2, "ii) Variance of X =");
disp(vY2, "Variance of Y =");
x = input("Type in the reference sequence (e.g. [1 2 3]): ");
y = input("Type in the second sequence (e.g. [3 2 1]): ");
r = correl(x, y);
plot2d3(r);
xlabel("Lag");
ylabel("Correlation");
title("Cross-Correlation between X and Y");

```

__OUTPUT GRAPH:__

![WhatsApp Image 2025-11-10 at 15 52 17_612a4f0b](https://github.com/user-attachments/assets/12d7570b-ae21-42dd-9298-4d9153b99900)


__RESULT:__

Thus the mean and variance using scilab code with the given reference sequence is verified and proved successfully.
