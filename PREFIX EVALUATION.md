# Ex.No:7D PREFIX EVALUATION

## AIM  
To write a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction.


## ALGORITHM

1. **Start the program.**
2. Define a set of valid operators: `*, -, +, %, /, **`.
3. Initialize an empty stack.
4. Traverse the prefix expression from **right to left**:
   - If the character is a **digit**, convert it to an integer and push it onto the stack.
   - If the character is an **operator**, pop two elements from the stack.
     - Apply the operator on the two popped operands.
     - Push the result back onto the stack.
   - If an invalid character is encountered, raise an error.
5. After traversal, the stack should contain only **one element**.
6. Return the **single element** as the evaluation result.
7. **End the program.**

## PROGRAM

```
OPERATORS=set(['*','-','+','*']) 

def evaluate(expression):
	stack = []
	for i in expression[::-1]:
	    if i not in OPERATORS:
	        stack.append(int(i))
	    else:
	       a=stack.pop()
	       b=stack.pop()
	       if i=='+':
	           stack.append(a+b)
	       elif i=='-':
	           stack.append(a-b)
	       elif i=='/':
	           stack.append(a/b)
	       elif i=='*':
	           stack.append(a*b)
	return stack.pop()
    
    
test_expression = input()
print(f"Prefix Expression : {test_expression}")
print(f"Evaluation result : {evaluate(test_expression)}")

```

## OUTPUT
![Screenshot 2025-05-19 113921](https://github.com/user-attachments/assets/0ff475f9-59c3-4d4e-a831-fa57cfd4ee3b)

![Screenshot 2025-05-19 113927](https://github.com/user-attachments/assets/ef0203d8-3b57-4ad5-8ab3-fa26854745fa)


## RESULT
Thus a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction has been successfully implemented.
