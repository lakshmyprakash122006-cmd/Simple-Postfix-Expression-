# Simple-Postfix-Expression-
Data structure practical program 
# Postfix Expression Evaluation using Stack

stack = []

exp = input("Enter postfix expression: ")

for ch in exp:
    if ch.isdigit():
        stack.append(int(ch))
    else:
        b = stack.pop()
        a = stack.pop()

        if ch == '+':
            stack.append(a + b)
        elif ch == '-':
            stack.append(a - b)
        elif ch == '*':
            stack.append(a * b)
        elif ch == '/':
            stack.append(a / b)

result = stack.pop()
print("Result:", result)
output:
Enter postfix expression: 23+
Result: 5
