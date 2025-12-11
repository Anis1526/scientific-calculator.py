# scientific-calculator.py
import math

def scientific_calculator():
    print("===== Scientific Calculator =====")
    print("Choose an operation:")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5. Power (a^b)")
    print("6. Square Root")
    print("7. Logarithm (base 10)")
    print("8. Natural Log (ln)")
    print("9. Sine (sin)")
    print("10. Cosine (cos)")
    print("11. Tangent (tan)")
    print("12. Factorial")
    print("13. Exit")

    while True:
        choice = input("\nEnter your choice: ")

        if choice == '13':
            print("Exiting... Goodbye!")
            break

        # Binary operations (need two numbers)
        if choice in ['1', '2', '3', '4', '5']:
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))

            if choice == '1':
                print("Result:", a + b)
            elif choice == '2':
                print("Result:", a - b)
            elif choice == '3':
                print("Result:", a * b)
            elif choice == '4':
                if b == 0:
                    print("Error: Cannot divide by zero!")
                else:
                    print("Result:", a / b)
            elif choice == '5':
                print("Result:", pow(a, b))

        # Single number operations
        else:
            num = float(input("Enter a number: "))

            if choice == '6':
                print("Result:", math.sqrt(num))
            elif choice == '7':
                print("Result:", math.log10(num))
            elif choice == '8':
                print("Result:", math.log(num))
            elif choice == '9':
                print("Result:", math.sin(math.radians(num)))
            elif choice == '10':
                print("Result:", math.cos(math.radians(num)))
            elif choice == '11':
                print("Result:", math.tan(math.radians(num)))
            elif choice == '12':
                print("Result:", math.factorial(int(num)))
            else:
                print("Invalid choice! Try again.")

# Run the calculator
scientific_calculator()

