# Octave

## Commands
###### clear all the figures
```octave
clear; close all; clc
```

## Symbols
```octave
: = range % e.g.: 1:4 = 1 2 3 4
```

## Vectors
```octave
v = [1; 2; 3; 4] % 1 X 4 vector
```

## Matrix
```octave
m1 = [1 2; 3 4] % 2 X 2 matrix
m2 = [1:4; 3:6] % 2 X 4 matrix

%% transpose
m1'

%% inverse
pinv(m1)
```

## Plot
```octave
%% define data
x = [1 2; 1 2];
y = [1 1];

%% plot
plot(x, y);

%% add markers
plot(x, y, 'rx');
```
