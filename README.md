
Matlab code snippets

# General

```Matlab
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
