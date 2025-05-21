# Ex.No:7A CONVERSION OF INFIX TO POSTFIX

## AIM  
To Write a Python program to convert given Infix expression to Postfix expression by following the precedence and associative rule. 
The input expression contains only  ^ and * . Use dictionary to set the priority for operators. Use set to hold the operators used in the given expression.


## ALGORITHM

1. Initialize an empty stack for operators and an empty string for output (postfix expression).
2. Scan the infix expression from left to right.
3. For each character in the expression:
4. If it's an operand (not in Op), append it to the output.
5. If it's '(', push it onto the stack.
6. If it's ')', pop from the stack and append to output until '(' is found. Discard '('.
7. If it's an operator (* or ^), then: While stack is not empty and top of stack is not '(' and precedence of current operator is less than or equal to the precedence of the top of the stack: Pop from stack and append to output.
8. Push current operator onto stack.
9. After scanning, pop and append all remaining operators from the stack to the output.
10. Return the postfix expression.


## PROGRAM

```
give me algorthim for this program                                                                                                                 Op = set(\['*','(','^',')'])
pr= {'*':1,'(':2,'^':3,')':4}

def infixToPostfix(exp):

stack = [] 
otp = '' 

for char in exp:
    if char not in Op:
        otp+=char
    elif char=='(':
        stack.extend('(')
    elif char==')':
        while stack and stack[-1]!='(':
            otp+=stack.pop()
        stack.pop()
    else:
        while stack and stack[-1]!='('and pr[char]<=pr[stack[-1]]:
            otp+=stack.pop()
        stack.append(char)
while stack:
    otp+=stack.pop()# Write your code here

return otp

exp =input()
print('infix notation: ',exp)

print('postfix notation: ',infixToPostfix(exp))

```

## OUTPUT
![Screenshot 2025-05-18 143939](https://github.com/user-attachments/assets/cff07070-1ac2-4336-9b0a-3de40151ded2)

## RESULT
Thus  a Python program to convert given Infix expression to Postfix expression by following the precedence and associative rule has been successfully implemented.

