# Octave

## Commands
###### clear all the figures
```octave
clear ; close all; clc
```

## Symbols
```octave
: = range, e.g.: 1:4 = 1 2 3 4
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

## Cost function
data = load('ex1data1.txt');
X = data(:, 1); y = data(:, 2);
m = length(y);
X = [ones(m, 1), data(:,1)];

theta = zeros(2, 1);



h_theta = X * theta
quadratic_diff = (h_theta - y) .^ 2;
J = 1/(2*m) * sum(quadratic_diff);

## Gradient descent
for iter = 1:num_iters
    diff = X * theta - y;
    x_diff = diff * X(iter, 2);
    theta = theta - ((alpha / m) * sum(x_diff))
end

## Feature normalization
std(X(:,2))

mu    = mean(X)
sigma = std(X)

indicies = 1:size(X, 2);

for i = indicies,
  XminusMu  = X(:, i) - mu(i);
  X_norm(:, i) = XminusMu / sigma(i);
end

## plot
plot(X, y, 'rx', 'MarkerSize', 10);
