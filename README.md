%% 
clc;
clear;


arr = 1:100;  
n = length(arr);
low =  1;
high = n;
fprintf('Think of a number between 1 and 100.\n');


while low <= high
    mid = floor((low + high)/2);
    guess = arr(mid);
    user_input = input(sprintf('Is your number %d? (Enter Yes(=), gtater than(>) , or less than(<)): ', guess), 's');
    
    if user_input == '='
        fprintf('Yay! Your number is %d.\n', guess);
        break;
    elseif user_input == '<'
        high = mid - 1;
    elseif user_input == '>'
        low = mid + 1;
    else
        disp('Invalid input. Please enter =, <, or >');
    end
end
