# Matlab code to variate color depending on a second value (y) or a third value (z) in a 2D plot


```
clear; close all; clc;

% Your Data
x = 0:0.01:10;
y = sin(x);


% 2D plot depending on y

% find indices 
indx1= find((y<0.2));
indx2= find((y>=0.2) & (y<0.5));
indx3= find((y>=0.5));

line1=y;
line2=y;
line3=y;

line1(indx2)=NaN;
line1(indx3)=NaN;

line2(indx1)=NaN;
line2(indx3)=NaN;

line3(indx1)=NaN;
line3(indx2)=NaN;

figure
plot(x,line1,'r',x,line2,'g',x,line3,'bl');

% 2D plot depending on z

z= cos(x);

% find indices 

indx1= find((z<0.2));
indx2= find((z>=0.2) & (z<0.5));
indx3= find((z>=0.5));

line1=y;
line2=y;
line3=y;

line1(indx2)=NaN;
line1(indx3)=NaN;

line2(indx1)=NaN;
line2(indx3)=NaN;

line3(indx1)=NaN;
line3(indx2)=NaN;

figure
plot(x,line1,'r',x,line2,'g',x,line3,'bl');
```
