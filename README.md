
Matlab code snippets
```Matlab
% Hello World
fprintf('Hello World!\n');

% Hello World to File
fid = fopen('hello.txt', 'w');
fprintf(fid,'Hello World!\n');
fclose(fid);

% Check if a file exists
if ~exist('hello.txt', 'file')
    % nope, does not exist
else
    % yep, exists
end
```

# General

```Matlab
%% Random numbers

% Seeding the RNG
rng(0, 'twister');

 % random number in [0..1]
rand
%> 0.1711

% random number in [a..b]
(b-a) * rand + a
%> a = -5
%> b = 5
%> -4.6740


%% Sampling integers from [1..10]
randi([1 10])
%> 4

randi([1 10],3)
%>   5     6     9
%>   4     8     7
%>  10     9     9

randi([1 10],[2 4])
%>   4     4     1     6
%>   3     3     5     8

%% Sampling from sequence
a = 1:6; 
datasample(a,1) % get random element
%>  2
datasample(a, 5, 'Weights', [1 1 1 2 2 3]) % with weights
%>  4     6     5     6     5
datasample(a, 5, 'Replace', false) % without replacement
%>  5     6     4     2     3
a(randperm(length(a))) % shuffle array
%>  2     1     4     6     5     3  
``` 

# Graphs
```Matlab
% Generate graph from matrix
m = randi([0 1], 10) % example: with 50% edges
G = graph(m, 'upper', 'OmitSelfLoops'); % upper = only upper triangle will be used
                                        % OmitSelfLoops = diagonal will be treated as zeros
``` 
