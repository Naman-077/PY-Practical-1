# PY-Practical-1
import math

# Function to find the roots of a quadratic equation
def find_roots(a, b, c):
    d = b**2 - 4*a*c  # Calculate the discriminant
    if d > 0:
        r1 = (-b + math.sqrt(d)) / (2 * a)
        r2 = (-b - math.sqrt(d)) / (2 * a)
        print("Roots are real and distinct:", r1, r2)
    elif d == 0:
        r = -b / (2 * a)
        print("Roots are real and equal:", r)
    else:
        print("Roots are not real")

# Input
try:
    a, b, c = map(float, input("Enter the coefficients a, b, c separated by commas: ").split(','))
    if a == 0:
        print("Coefficient 'a' cannot be zero for a quadratic equation.")
    else:
        find_roots(a, b, c)
except ValueError:
    print("Invalid input. Please enter numeric values for a, b, and c.")
