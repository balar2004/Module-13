# Exp.No:32  
## CONVERSION OF INFIX TO POSTFIX

---

### AIM  
To write a Python program to convert a given Infix expression to Postfix expression by following the precedence and associative rules. The input expression contains only Division, Subtraction, and Bitwise AND operators. A dictionary is used to set the priority for operators, and a set is used to hold the operators used in the given expression.

---

### ALGORITHM

1. **Start the program.**
2. **Initialize an empty stack** and an empty output string.
3. **Iterate through each character** in the infix expression:
   - If the character is **not an operator**, append it directly to the output string.
   - If the character is an **open parenthesis '('**, push it onto the stack.
   - If the character is a **close parenthesis ')'**, pop from the stack and append to the output until encountering a left parenthesis '('.
   - If the character is an **operator**, handle it based on precedence:
     - While there’s an operator at the top of the stack with higher or equal precedence, pop the stack and append those operators to the output.
     - Push the current operator onto the stack.
4. **Use a priority dictionary** to define operator precedence, ensuring higher precedence operators are placed before lower precedence ones.
5. Once the expression is fully processed, continue popping any remaining operators from the stack and append them to the output.
6. **Return the final postfix expression.**
7. **Print the result.**
8. **End the program.**

---

### PROGRAM

```
Operators = set(['+', '-', '*', '/', '(', ')', '^'])  
Priority = {'+':1, '-':1, '*':2, '/':2, '^':3, '(':0, ')':0} 
stack = [] 
output = []
 
def infixToPostfix(expression):
    for char in expression:
        if char not in Operators:
            output.append(char)
            
        elif char == '(':
            stack.append(char)
            
        elif char == ')':
            while (stack and stack[-1]!='('):
                output.append(stack.pop())
            stack.pop()
            
        else:
            while stack and Priority[char] <= Priority[stack[-1]]:
                output.append(stack.pop())
            stack.append(char)


    while stack:
        output.append(stack.pop())
    
    return ''.join(output)
    
expression = input()
print("Infix notation: ",expression)
print("Postfix notation: ",infixToPostfix(expression))
```

### OUTPUT
![Screenshot 2025-05-04 235547](https://github.com/user-attachments/assets/d699a6b0-d6e6-4465-b23f-b56a729eb538)


### RESULT
Thus,the python program to convert a given Infix expression to Postfix expression by following the precedence and associative rules has been executed and verified successfully.
