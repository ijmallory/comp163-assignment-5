# comp163-assignment-5
# Challenge 1: Number Sequence Generator
print("=== Challenge 1: Collatz Conjecture ===")
current_number = int(input("Enter starting number: "))
step_count = 0
print("Sequence:", current_number, end=" ")

while current_number != 1:
    if current_number % 2 == 0:
        current_number = current_number // 2
    else:
        current_number = (current_number * 3) + 1
    print(current_number, end=" ")
    step_count += 1
print()
print("Steps:", step_count)
print()

# Challenge 2: Prime Number Checker
print("=== Challenge 2: Prime Number Checker ===")
number = int(input("Enter a number: "))

if number > 1:
    print(f"Testing divisors from 2 to {number - 1}...")
    for i in range(2, number - 1):
        if number % i == 0:
            print(f"{number} is not prime (divisible by 3)")
            break
    else:
        print(f"{number} is prime!")
print()

# Challenge 3: Multiplication Table Grid
print("=== Challenge 3: Multiplication Table ===")
print("Multiplication Table:")
print("  ", end="")

# For loop for headline numbers
for headline in range(1, 11): #The range functions used below start at 1 and since 11 is not included, it's from 1 to 10
    print(f"{headline:4}", end="")
print()

# For loop to display the rows, columns, and products for the Multiplication Grid/Table
for row in range(1, 11):
    print(f"{row:2}", end=" ")
    for column in range(1, 11):
        table_val = row * column
        print(f"{table_val:3}", end=" ")
    print()
