def iterative_factorial(n):
    """Calculates n! iteratively using a loop."""
    if n == 0:
        return 1
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result

def recursive_factorial(n):
    """Calculates n! recursively."""
    if n == 0:
        return 1
    # Base case: Factorial of 0 is 1
    return n * recursive_factorial(n - 1)
    # Recursive step: n! = n * (n-1)!

# --- List of numbers to test ---
numbers = [0, 5, 10, 25, 50, 100]

# --- 1. Iterative Results ---
print("Factorial results using an iterative function")
for n in numbers:
    result = iterative_factorial(n)
    print(f"{n}! = {result}")

# --- 2. Recursive Results ---
print("\nFactorial results using a recursive function")
for n in numbers:
    result = recursive_factorial(n)
    print(f"{n}! = {result}")

# The original output image shows "Press any key to continue..." 
# This is a common feature in command-line environments, 
# but isn't a standard Python command. We can simulate a pause 
# that requires user input to exit, if desired.
# input("\nPress any key to continue . . .")
