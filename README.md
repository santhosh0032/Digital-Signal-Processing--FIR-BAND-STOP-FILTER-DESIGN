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
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1=');
Wc2=input('enter the value of Wc2=');
N=input('enter the value of N=');
alpha=(N-1)/2;
eps=0.001;
%Band Pass Filter Coefficient
n=0:1:N-1;
hd=(sin(Wc1*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)
%Blackman Window Sequence
n=0:1:N-1;
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(N-1))
hn=hd.*wh
% Plot the Band Stop Filter with Blackman Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
~~~

## OUTPUT:
<img width="1449" height="1286" alt="image" src="https://github.com/user-attachments/assets/bd3b11e8-6414-4788-8c90-e263328f6ed9" />


## RESULT:
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
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1=');
Wc2=input('enter the value of Wc2=');
N=input('enter the value of N=');
alpha=(N-1)/2;
eps=0.001;
%Band Pass Filter Coefficient
n=0:1:N-1;
hd=(sin(Wc1*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)
%Blackman Window Sequence
n=0:1:N-1;
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(N-1))
hn=hd.*wh
% Plot the Band Stop Filter with Blackman Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
~~~

## OUTPUT:
![WhatsApp Image 2026-04-01 at 11 39 08 AM (1)](https://github.com/user-attachments/assets/17a2066c-620d-4c11-aa63-8bfcae2160bc)


## RESULT:
<img width="1244" height="481" alt="image" src="https://github.com/user-attachments/assets/5fe69ee2-3ede-40b3-8342-9f04b74f0976" />
