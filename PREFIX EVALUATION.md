# Exp.No:34  
## PREFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction.

---

### ALGORITHM

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

---

### PROGRAM

```
#Reg.NO-212223060119
#Name-Kavindra T G
OPERATORS = {'+', '-', '*', '/', '%', '**'}

def evaluate_prefix(expression):
    stack = []
    tokens = expression.split()[::-1]

    for token in tokens:
        if token not in OPERATORS:
            stack.append(int(token))
        else:
            a = stack.pop()
            b = stack.pop()
            if token == '+':
                result = a + b
            elif token == '-':
                result = a - b
            elif token == '*':
                result = a * b
            elif token == '/':
                result = a / b
            elif token == '%':
                result = a % b
            elif token == '**':
                result = a ** b
            stack.append(result)
    
    return stack[0]

prefix_expr = input("Enter prefix expression (e.g., '+ 3 * 4 2'): ")
print("Prefix Expression:", prefix_expr)
print("Evaluated Result:", evaluate_prefix(prefix_expr))


```


### OUTPUT
![image](https://github.com/user-attachments/assets/0778242f-2b21-40b0-ae90-3c9ff9bc0cb3)



### RESULT
Thus, the python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction has been executed and verified successfully.
