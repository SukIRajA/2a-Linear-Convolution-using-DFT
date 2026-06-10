EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION

```
clc;
clear;
x = [10 10 10 10];
h = [2 4 6 8];
m = length(x);
n = length(h);
a = 0:m-1;
b = 0:n-1;
subplot(3,1,1);
plot2d3(a, x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b, h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
y = zeros(1, m+n-1);
for i = 1:(m+n-1)
conv_sum = 0;
for j = 1:i
if ((j <= m) & ((i-j+1) <= n))
conv_sum = conv_sum + x(j) * h(i-j+1);
end
end
y(i) = conv_sum;
end
disp(y, 'Convolution Sum using Direct Formula Method = ');
subplot(3,1,3);
t = 0:(m+n-2);
plot2d3(t, y);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Output Signal y');
```




### CALCULATIONS:

<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/e687ff97-3e88-4b95-a9eb-df9b90b0995a" />

<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/f58fa4f9-f032-4b8c-b410-ebb36f179785" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/710d2c6c-dc1b-4498-a7b8-326526c908e3" />

<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/f7a29cc9-b339-428a-a815-354f533511c1" />
<img width="1600" height="1425" alt="image" src="https://github.com/user-attachments/assets/9ee2cddb-28dd-47b8-8bc4-04ea203d736c" />



### SAMPLE OUTPUT:
<img width="1478" height="1600" alt="image" src="https://github.com/user-attachments/assets/04f43b5a-9c34-4378-bc5c-92c074ca83be" />



<img width="1600" height="567" alt="image" src="https://github.com/user-attachments/assets/93375d8d-6143-42ce-8af3-e8b3e843a36e" />


RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
