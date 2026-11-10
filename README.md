# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
```
clc; 
clear;
x=[1 2 3 4];
n1=0:1:length(x)-1;
subplot(3,1,1);
plot2d3(n1,x);
xlabel('time');
ylabel('amplitude');
title('input sequence');
h=[2 4 8 6];
n2=0:1:length(h)-1;
subplot(3,1,2);
plot2d3(n2,h);
xlabel('time');
ylabel('amplitude');
title('impulse sequence');
N1=length(x);
N2=length(h);
N=max(N1,N2);
N3=N1-N2;
if(N3>0)
h=[h,zeros(1,N3)];
else
x=[x,zeros(1,abs(N3))];
end
disp(x)
disp(h)
for n=1:N
y(n)=0;
for i=1:N
j=n-i+1;
if(j<=0)
j=N+j;
end
y(n)=y(n)+x(i)*h(j);
end
end
disp(y)
n=0:N-1;
subplot(3,1,3);
plot2d3(n,y);
xlabel('time');
ylabel('amplitude');
title('circular convolution');
```

### CALCULATIONS:

<img width="1309" height="1599" alt="WhatsApp Image 2026-11-10 at 5 35 10 PM" src="https://github.com/user-attachments/assets/1f082172-1ad3-4f39-aa56-753a593fc3f0" />

### SAMPLE OUTPUT:

<img width="1599" height="1138" alt="WhatsApp Image 2026-11-10 at 11 14 44 AM" src="https://github.com/user-attachments/assets/2e96b266-1b7f-4168-837f-07f4b50bcd37" />




## RESULT:
Thus, the circular convolution of the two given sequences were performed and its result was verified.

