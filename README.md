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
clc; clear; close;

// ================= Mean Calculation =================

// PDF: z = 3*(1-x)^2

function X = f(x)
    X = x * 3*(1-x)^2;
endfunction

a = 0; b = 1;
EX = intg(a, b, f);

function Y = c(y)
    Y = y * 3*(1-y)^2;
endfunction

EY = intg(a, b, c);

disp("i) Mean of X = " + string(EX));
disp("ii) Mean of Y = " + string(EY));


// ================= Variance Calculation =================

function X = g(x)
    X = x^2 * 3*(1-x)^2;
endfunction

EX2 = intg(a, b, g);

function Y = h(y)
    Y = y^2 * 3*(1-y)^2;
endfunction

EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp("iii) Variance of X = " + string(vX2));
disp("iv) Variance of Y = " + string(vY2));


// ================= Cross Correlation =================

x = input("Enter reference sequence x = ");
y = input("Enter sequence y = ");

n1 = max(size(y)) - 1;
r = corr(x, y, n1);

plot2d3('gnn', r);
xlabel("Lag");
ylabel("Correlation Value");
title("Cross Correlation Plot");

```
__Calculation:__


![WhatsApp Image 2025-11-23 at 06 49 36_39d78650](https://github.com/user-attachments/assets/5a09aba0-df33-4cf0-bfdf-38bc14408f15)


__OUTPUT GRAPH:__

![WhatsApp Image 2025-11-23 at 06 49 51_82e9e344](https://github.com/user-attachments/assets/fc57e2db-025d-4be8-819e-2e91ed485ac7)
![WhatsApp Image 2025-11-23 at 06 50 05_e1e2fcd1](https://github.com/user-attachments/assets/b3502e1e-2929-4c69-b583-9e9a1e9a67b2)



__RESULT:__

Thus the program for mean, variance and cross correlation in SCILAB and output is veified.

