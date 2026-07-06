# Cos202
Practical 
import math

print("====================================")
print("     MATHEMATICAL CALCULATOR")
print("====================================")

while True:
    print("\nChoose an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Power (^)")
    print("6. Square Root (√)")
    print("7. Modulus (%)")
    print("8. Percentage")
    print("9. Clear")
    print("10. OFF")

    choice = input("Enter your choice (1-10): ")

    if choice == "10":
        print("Calculator OFF. Goodbye!")
        break

    elif choice == "9":
        print("\n" * 50)
        continue

    elif choice == "6":
        num = float(input("Enter a number: "))
        if num >= 0:
            print("Square Root =", math.sqrt(num))
        else:
            print("Cannot calculate square root of a negative number.")

    elif choice == "8":
        num = float(input("Enter the number: "))
        total = float(input("Enter the total value: "))
        percentage = (num / total) * 100
        print("Percentage =", percentage, "%")

    elif choice in ["1", "2", "3", "4", "5", "7"]:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if choice == "1":
            print("Answer =", num1 + num2)

        elif choice == "2":
            print("Answer =", num1 - num2)

        elif choice == "3":
            print("Answer =", num1 * num2)

        elif choice == "4":
            if num2 != 0:
                print("Answer =", num1 / num2)
            else:
                print("Division by zero is not allowed.")

        elif choice == "5":
            print("Answer =", num1 ** num2)

        elif choice == "7":
            print("Answer =", num1 % num2)

    else:
        print("Invalid choice. Try again.")
