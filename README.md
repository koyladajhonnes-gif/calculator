# calculator
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error! Division by zero is not allowed."
    return a / b
def calculator():
    print("===== Simple Calculator CLI =====")
    print("Operations: +  -  *  /")
    print("Type 'exit' to quit.\n")

    while True:
        operation = input("Enter operation (+, -, *, /): ").strip()

        if operation.lower() == 'exit':
            print("Exiting Calculator... Goodbye! 👋")
            break

        if operation not in ['+', '-', '*', '/']:
            print("Invalid operation! Please enter one of +, -, *, /.\n")
            continue

        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input! Please enter numeric values.\n")
            continue

        if operation == '+':
            result = add(num1, num2)
        elif operation == '-':
            result = subtract(num1, num2)
        elif operation == '*':
            result = multiply(num1, num2)
        elif operation == '/':
            result = divide(num1, num2)

        print(f"Result: {result}\n")
if _name_ == "_main_":
    calculator()
