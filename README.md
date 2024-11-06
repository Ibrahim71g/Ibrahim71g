# Define a function to check if a number is prime
def is_prime(num):
    # Edge cases: numbers less than 2 are not prime
    if num < 2:
        return False
    
    # Check if the number has any divisors other than 1 and itself
    for i in range(2, int(num**0.5) + 1):  # Only go up to the square root of the number
        if num % i == 0:  # If num is divisible by i, it's not a prime
            return False
    
    # If no divisors were found, the number is prime
    return True

# Test the function with some numbers
test_numbers = [1, 2, 3, 4, 5, 10, 13, 17, 19, 20]

# Check each number and print whether it's prime or not
for number in test_numbers:
    if is_prime(number):
        print(f"{number} is a prime number.")
    else:
        print(f"{number} is not a prime number.")
