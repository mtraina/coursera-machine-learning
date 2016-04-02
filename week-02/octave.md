# Octave

## Symbols
: = range, e.g.: 1:4 = 1 2 3 4

## Matrix
[1:4; 3:6]

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
std(X(:,1))

## plot
plot(X, y, 'rx', 'MarkerSize', 10);
