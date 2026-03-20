# EXP 6 : SIMULATION-OF-MULTIRATE-DSP-WITHOUT-FUNCTION

## AIM: 

To perform and verify multirate DSP without function using SCILAB.

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM : 
```
clear; 
clc; 
close; 
n = 0:%pi/50:2*%pi; 
x = sin(%pi*n); //original signal 
M=input('Enter the downsampling factor'); 
L=input('Enter the upsampling factor'); 
//Down Sampling 
downsampling_x = x(1:M:length(x)); 
disp(x,'Input signal x(n)='); 
disp(downsampling_x,'Downsampled Signal'); 
figure(1); 
subplot(2,1,1) 
plot2d3(1:length(x),x); 
xtitle('original singal') 
subplot(2,1,2) 
plot2d3(1:length(downsampling_x),downsampling_x); 
xtitle('Downsampled Signal by a factor of M'); 
//Upsampling 
upsampling_x=[]; 
for i=1:length(x) 
upsampling_x(1,L*i)=x(i); 
end 
disp(x,'Input signal x(n)='); 
disp(upsampling_x,'Upsampled Signal');
figure(2); 
subplot(2,1,1); 
plot2d3(x); 
title('original signal'); 
subplot(2,1,2); 
plot2d3(upsampling_x); 
title('Upsampled Signal by a factor of L');
```

## OUTPUT: 

<img width="1221" height="247" alt="image" src="https://github.com/user-attachments/assets/b70b1d3a-ff48-4510-acb6-2852f7e3fdbf" />
<img width="1917" height="1076" alt="image" src="https://github.com/user-attachments/assets/3c45632c-8909-42c1-befb-28e6d2dd03bf" />
<img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/2ce34578-e43a-4f01-943c-6d65f1d06808" />




## RESULT: 
Thus the decimation process by a factor M and interpolation process by a factor L using 
SCILAB was implemented. 
