# intro-to-python
def basic_calculator():
    """A simple calculator program that performs basic arithmetic operations."""
    try:
        num1_str = input("Enter the first number: ")
        num1 = float(num1_str)  # Convert to float to handle decimals

        num2_str = input("Enter the second number: ")
        num2 = float(num2_str)  # Convert to float

        operation = input("Enter the operation (+, -, *, /): ")

        if operation == '+':
            result = num1 + num2
            print(f"{num1} + {num2} = {result}")
        elif operation == '-':
            result = num1 - num2
            print(f"{num1} - {num2} = {result}")
        elif operation == '*':
            result = num1 * num2
            print(f"{num1} * {num2} = {result}")
        elif operation == '/':
            if num2 == 0:
                print("Error: Cannot divide by zero.")
            else:
                result = num1 / num2
                print(f"{num1} / {num2} = {result}")
        else:
            print("Invalid operation. Please enter +, -, *, or /.")

    except ValueError:
        print("Invalid input. Please enter valid numbers.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

if __name__ == "__main__":
    basic_calculator()
