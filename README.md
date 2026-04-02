# Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1=');
Wc2=input('enter the value of Wc2=');
N=input('enter the value of N=');
alpha=(N-1)/2;
eps=0.001;
%Band Stop Filter Coefficient
n=0:1:N-1;
hd=(sin(Wc1*(n-alpha+eps))+sin(pi*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))/(pi*(n-alpha+eps))
%Bartlett Window Sequence
n=0:1:N-1;
wh=1−2∗𝑎𝑏𝑠(𝑛−𝑎𝑙𝑝ℎ𝑎)𝑁
hn=hd.*wh
% Plot the Band Stop Filter with Bartlett window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="1600" height="948" alt="image" src="https://github.com/user-attachments/assets/75685687-92c4-4853-8b33-243ac803cd73" />


## RESULT:
<img width="1599" height="488" alt="image" src="https://github.com/user-attachments/assets/99ba5aba-67e6-4e01-b247-a4750cfb6506" />

