# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
~~~
clc; % clear screen
clear all; % clear workspace
close all; % close all figure windows

Wc1 = input('enter the value of Wc1=');
Wc2 = input('enter the value of Wc2=');
N = input('enter the value of N=');

alpha = (N-1)/2;
eps = 0.001;

% Band Stop Filter Coefficient
n = 0:1:N-1;
hd = (sin(pi*(n-alpha+eps)) - sin(Wc2*(n-alpha+eps)) + sin(Wc1*(n-alpha+eps))) ...
     ./ (pi*(n-alpha+eps));

% Bartlett Window Sequence
n = 0:1:N-1;
wh = 1 - (2*abs(n-alpha)/N);

% Windowed impulse response
hn = hd .* wh;

% Plot the Band Stop Filter with Bartlett Window Technique
w = 0:0.01:pi;
h = freqz(hn,1,w);

plot(w/pi, abs(h), 'blue');
xlabel('Normalized Frequency');
ylabel('Magnitude');
title('Band Stop Filter using Bartlett Window');
grid on;
~~~

## OUTPUT:
![WhatsApp Image 2026-04-01 at 11 39 08 AM (1)](https://github.com/user-attachments/assets/61e76089-8f8d-4108-b3c8-5b43f0442848)


## RESULT:
![WhatsApp Image 2026-04-01 at 10 34 22 PM](https://github.com/user-attachments/assets/feb5d5b0-6bb1-4036-8c83-1aaf06c9224d)

