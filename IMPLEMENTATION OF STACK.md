# Ex.No:7B IMPLEMENTATION OF STACK


## AIM  
To write a Python program to implement a stack using a list and its built-in methods (`append()`, `pop()`).


## ALGORITHM

1. **Start the program.**
2. **Define a class `st`** with the following methods:
   - `push(self, num)`: Adds the number `num` to the stack.
   - `pop(self)`: Removes and returns the top element from the stack.
3. **Create a stack object `s`** using the class `st`.
4. **Input the stack size**: Take an integer input `size` to define the size of the stack.
5. **Loop through numbers from 1 to size**: Add only the odd numbers to the stack using the `push()` method.
6. **Display the elements** in the stack after the loop completes.
7. **Call `pop()`** to remove the top element from the stack and display the popped element.
8. **Display the stack again** to show the remaining elements.
9. **End the program.**

---

## PROGRAM

```
stack = []
for i in range(3):
    a=input()
    stack.append(a)
print("Stack before elements are popped")
print(stack)

for i in range(3):
    stack.pop()
print("\nStack after elements are popped:")
print(stack)

```
## OUTPUT 
![Screenshot 2025-05-19 113412](https://github.com/user-attachments/assets/b8308dfd-b452-4658-9748-63eb830543fe)

## RESULT
Thus a Python program to implement a stack using a list and its built-in methods (`append()`, `pop()`) has been successfully implemented.
