# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

## AIM: 

 To Obtain DFT and FFT of a given sequence in SCILAB. 

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM: 
```
clc;
clear;
close;

x = [1,2,3,4,5,3,2,6];   // You can change this sequence
N = length(x);

X_dft = zeros(1, N);
for k = 0:N-1
    for n = 0:N-1
        X_dft(k+1) = X_dft(k+1) + x(n+1)*exp(-%i*2*%pi*k*n/N);
    end
end

X_fft = fft(x, -1);   // -1 for forward FFT in Scilab

disp("Input sequence x = "), disp(x);
disp("DFT of x = "), disp(X_dft);
disp("FFT of x = "), disp(X_fft);
```

## OUTPUT: 

<img width="1221" height="559" alt="Screenshot 2025-11-25 113006" src="https://github.com/user-attachments/assets/717fc893-ecd8-4e5b-8af8-205a3633634a" />


## RESULT: 

DFT and FFT of a given sequence in SCILAB was obtained.
